---
title: How to queue many jobs and play nice with others on the cluster (Viper)
date: 2014-10-01T12:13:47+00:00
author: Chongle Pan
layout: default
parent: 2014 posts
grand_parent: Posts
---
This is a guest post from Doug Hyatt:

### Queuing Many Jobs {#queuing_many_jobs.sectionedit2}

<div class="level2">
  <p>
    Viper is a resource shared by many users. It is good form to consider the impact of your job submissions on the other users of the machine. While the queuing system can resolve most issues using priorities, if one user submits many long jobs while the machine is idle, he or she can take over the entire queue. If other users subsequently wish to run jobs, they can find themselves forced to wait many hours for the first user&#8217;s jobs to finish.
  </p>
  
  <p>
    One way in which a user can “play nice” with others is to only request 25-50% of the available cores, and use a shell script (or Python/Perl) to control their processes. Even if they wish to process 20,000 files, they can do so on a mere 100 processors, without submitting 20,000 long jobs to the queue. The easy way to do this is with the ”-t” option to PBS, i.e.
  </p>
  
  <pre class="code">#PBS -t 1-100
/my/scripts/script.py -id $PBS_ARRAYID -numtasks 100 -input /my/input/input.$PBS_ARRAYID.txt -output /my/outputs/output.$PBS_ARRAYID.txt</pre>
  
  <p>
    The range following the -t will specify the number of cores and the array ids. It will run one copy of the script on each core, passing it the id (which will be a number from 1-100). It also tries to get consecutive nodes if it can, which plays nice by using as few nodes as possible (each node = multiple cores).
  </p>
  
  <p>
    So, the above job will start “script.py” on 100 cores, where each one gets passed its id (“script.py -id 1”, “script.py -id 2”, etc.) If you have a single file, say, that contains a list of 20,000 files you want to process, you can easily divide the 20,000 files among your 100 scripts (since each script knows its id, you can access that id inside the script and determine which files to process).
  </p>
  
  <p>
    One useful method is to “stripe” a file using modulo arithmetic.
  </p>
  
  <pre class="code">#PBS -t 1-100
/my/scripts/script.py -id $PBS_ARRAYID -numtasks 100 -output /my/outputs/output.$PBS_ARRAYID.txt</pre>
  
  <p>
    (Note, if you want 200 cores and you change the top line to 1-200, you need to change the numtasks argument to your script to 200 as well. I don&#8217;t know of a PBS environment variable that contains this value).
  </p>
  
  <p>
    Inside the python script, one might read a file as follows:
  </p>
  
  <pre class="code"># parse arguments to get "id" and "numtasks", numtasks is 100 in this case
counter = 0
with open("process.files.list.txt", "r" as f):
    counter += 1
    data = f.readline()
    if id%numtasks == counter%numtasks:
        # some code to process this file</pre>
  
  <p>
    Same thing in Perl:
  </p>
  
  <pre class="code">counter = 0;
open FH, "process.files.list.txt" or die "couldn't open file";
while(data = &lt;FH&gt;) {
  counter++;
  if(id%numtasks == counter%numtasks) {
    # some code to process this file
  }
}
close FH;</pre>
  
  <p>
    This usually ensures more evenness among the data given to each core than if you gave the first 200 to one processor, second 200 to next processor, etc.(although this would still be better than queueing 20,000 jobs).
  </p>
  
  <p>
    The above can serve as a general template for running a large number of jobs using a smaller number of processors and is generally considered a best practice for allowing other users to access some nodes on the machine.
  </p>
</div>

### The Head Node {#the_head_node.sectionedit3}

<div class="level2">
  <p>
    It is important to remember that viper&#8217;s head node is <strong>not a compute resource</strong>. Loading the head node down with intensive compute tasks can lead to delays and headaches for other users. Best practice for any job with significant compute time is to submit it to the queuing system.
  </p>
</div>

### Threads, Processes, and Memory {#threads_processes_and_memory.sectionedit4}

<div class="level2">
  <p>
    Viper&#8217;s queuing system does not disable forks or multithreading. Although a single task is <strong>supposed</strong> to run on a single core, there is nothing to prevent a user from forking off new processes, or running code with multiple threads. It is considered poor form and a bad practice to spawn more processes than the queuing system expects. The best practice is to explicitly ask for a certain number of processors if you wish to perform multithreading.
  </p>
  
  <p>
    For example, suppose you want to run <strong>blastp</strong> on eight threads via a queue with 8 processors per node. Using PBS, you can do the following:
  </p>
  
  <pre class="code">#PBS -l nodes=1:ppn=8
/my/blast/blastp -query /my/nr/query_gene.faa -db /my/nr/nr -num_threads 8 &gt; /my/nr/output.txt</pre>
  
  <p>
    The ”-l” directive explicitly tells the queuing system that you would like this job to take a node and 8 processors on that node. By requesting 8 processors, the user can then spawn 8 threads without worrying about overloading the machine.
  </p>
  
  <p>
    The user should also remember that each node has its own memory (the smallest cores on viper have 8GB/node) which is shared among all its cores. If you spawn jobs as normal (one per core), but your jobs are expected to use substantially more than 1GB each, you may run into memory problems. The user should be aware if using the queue with these nodes in it of this memory limitation, and not submit jobs to the queue that will cause excessive paging or possibly crash the node. (One way around this is, if you must use this queue, to explicitly ask for an entire node per job, although this is obviously less efficient than simply running on a higher memory queue).
  </p>
</div>