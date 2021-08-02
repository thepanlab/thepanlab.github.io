Unifam User Manual 
 
======================================================================== 
Setup and Installation 

1. tar -xzvf Unifam.tar.gz  
Suppose the absolute path of Unifam package is *  
2. cd */Unifam/unifam_mm/ 
3. Search "hmmsearchPath" in "unifam_mm.cpp", Change the value of "hmmsearchPath" to "*/Unifam/bin/hmmsearch" 
4. cd */Unifam/unifam_mma/ 
5. Search "unifampath" in "unifam_mma.cpp", Change the value of unifampath to "*/ Unifam/unifam/src/UniFam.py" 
6. cd */Unifam/unifam_mm/Debug, type "make", it will generate a binary "unifam_mm" 
7. cd */Unifam/unifam_mma/Debug/", type "make", it will generate a binary "unifam_mma" 

NOTE: if the compilation failed, please try differnt compilers in Makefile. 
Remember to add execution permissions to the binaries in bin directory.
 
======================================================================== 
Guide to Annotate Proteins 

1. cd */Unifam/Package/pipelinetest 
Make sure the file of protein sequence is in the same folder of "samplesplit.sh", "samplemm.sh", "samplemma.sh", "samplecombine.sh".  
Rename the protein sequence file to "proteins.fasta" 
Split proteins 
2. Modify "samplesplit.sh". Provide the path of unifam to PATHUNIFAM.  
3. Submit "samplesplit.sh" by "qsub samplesplit.sh". 
Run MM 
4. Modify "samplemm.sh". Provide the path of unifam to PATHUNIFAM 
5. Submit "samplemm.sh" by "qsub samplemm.sh". 
Run MMA 
6. Modify "samplemma.sh". Modify "samplemm.sh". Provide the path of unifam to PATHUNIFAM 
7. Submit "samplemma.sh" by "qsub samplemma.sh". 
Combine 
8. Submit "samplecombine.sh" by "qsub samplecombine.sh". 
The annotated proteins will be in files "proteins.annot" and "proteins_annot.faa"
 
 
======================================================================== 
Help of unifam_mm: 
 
This is MPI version for unifam to do the hmmsearch distributedly, hmm models and proteins need to be both splitted accordingly, and have size information stored in two meta files respectively. 
 
[Usage] 
unifam_mm [options] -cpu <cores> -ih <file_dir_hmm> -ip <file_dir_proteins> -fh <meta_info_file_hmm> -fp <meta_info_file_protein> -od <out_directory>"  
 
[Inputs] 
Please don't put '\\' or '/' after the name of the directory 
-ih <file_dir_hmm> file directory for hidden markov models used for protein families   
-ip <file_dir_proteins> file directory for query protein chunks 
-fh <meta_info_file_hmm> file with meta information of hidden markov model chunks, file_name (tab) max_len (tab) min_len 
-fh <meta_info_file_hmm> file with meta information of protein chunk files, file_name (tab) max_len (tab) min_len 
-cpu <cores> mutlithreading numbers for hmmsearch 
 
[Outputs]    
-od <out_directory> output direcotry for hmmer search results 
 
======================================================================== 
Help of unifam_mma 
 
This is a MPI version of unifam to generate group file and annotations for each protein chunk after hmmsearch result, usually run after 'unifam_mm. 
 
[Usage]  
unifam_mma [options] -hd <folder_for_protein_hmmresult> -fd <proteinfasta_dir> -data <annotation_database> -dtype <database_type> -od <final_output_folder> 
 
[Inputs] 
Please don't put '\\' or '/' after the string of the directory 
-hd <folder_for_protein_hmmresult> this is folder of folders of protein chunks containing hmmsearch result * .domtab files 
-fd <proteinfasta_dir> protein sequence fasta files folder 
-data <annotation_database> this is the folder for annotation database downloaded from Uniprot 
-dtype <database_type> annotation type, eg. 'prok',''euk', 'all' 
 
Outputs of this program are: 
annotation file, group file, protein fasta file with annotated header 
They will be copied to the folder defined by [output]: 
-od <final_output_folder> directory for final annotation and other related files 
