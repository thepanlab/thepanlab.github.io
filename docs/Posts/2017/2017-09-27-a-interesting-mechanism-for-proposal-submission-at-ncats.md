---
layout: default
title: Development of intelligent agents for biomedical reasoning using knowledge graphs
date: 2017-09-27T15:02:14+00:00
author: Chongle Pan
parent: 2017 posts
grand_parent: Posts
---
We recently submitted a joint preproposal (title: Development of intelligent agents for biomedical reasoning using knowledge graphs) to to a NIH NCATS proposal call with Blair Christian, Mike Leuze and Larry Roberts. Since the call has been closed, I want to share our experience with this interesting mechanism used by NCATS to screen potential proposals. The call actually did not release the full text of the FOA publicly. The FOA is available only for applicants who successfully submitted the correct answer for the question below. I copied the text in blue below.

&nbsp;

<span style="color: #0000ff;">Thank you for your interest in the NCATS Translator Challenge. To register for the challenge, please solve the following hypothetical problem. POST your answer along with contact information (i.e., email and name) to this address https://ncats.io/challenge. (We leave it up to you to decide how you want to format your submission.) Note that you will only receive an email confirmation from us if you have successfully solved the problem; no email confirmations will be sent for incorrect or invalid submissions. You may submit your answer as often as you&#8217;d like. While there are no limits to the number and rate of submissions, please keep in mind the delay in email response as you make your submissions. Best of luck!</span>

<span style="color: #0000ff;">Beta-defensins are antimicrobial peptides that help prevent infections. An NCATS scientist by the name of Lothar, with a background in mathematics, has discovered how the strategic substitution of key amino acid residues of a beta-defensin peptide allows the peptide to target specific bacteria. To demonstrate this, he substituted 18 residues to produce the following peptide.</span>

<span style="color: #0000ff;">ICVIDLAVSISFNCLIRLPVVEGGIEDPVTCLKAGAICHIVFCPRRYKQIGVCGLPGTKCCKKP</span>

<span style="color: #0000ff;">In order for the peptide to work, the set of substituted residues (i.e., a ‘recognition signature’) must be recognized in a specific order, starting at a specific residue. In the moment that leads to his discovery, Lothar conjectures &#8220;all roads must lead to Rome&#8221; and proceeds to tabulate possible recognition signatures, starting at different peptide residues, as follows:</span>

<span style="color: #0000ff;">1: I</span>  
 <span style="color: #0000ff;">2: CI</span>  
 <span style="color: #0000ff;">3: VIDIVICI</span>  
 <span style="color: #0000ff;">4: ICI</span>  
 <span style="color: #0000ff;">5: DIVICI</span>  
 <span style="color: #0000ff;">6: LVIDIVICI</span>

<span style="color: #0000ff;">&#8230;.</span>

<span style="color: #0000ff;">12: FLVIDIVICI</span>  
<span style="color: #0000ff;">13: NIVIDIVICI</span>

<span style="color: #0000ff;">&#8230;.</span>

<span style="color: #0000ff;">20: VIDIVICI</span>  
<span style="color: #0000ff;">21: VPLIVICI</span>

<span style="color: #0000ff;">&#8230;.</span>

<span style="color: #0000ff;">59: ^^^NOT A VALID SIGNATURE^^^</span>  
<span style="color: #0000ff;">60: ^^^NOT A VALID SIGNATURE^^^</span>  
<span style="color: #0000ff;">61: ^^^NOT A VALID SIGNATURE^^^</span>  
<span style="color: #0000ff;">62: ^^^NOT A VALID SIGNATURE^^^</span>  
<span style="color: #0000ff;">63: ^^^NOT A VALID SIGNATURE^^^</span>  
<span style="color: #0000ff;">64: PLIVICI</span>

<span style="color: #0000ff;">Can you identify the missing 18-residue signature necessary for target recognition by this peptide?</span>

&nbsp;

I initially thought all the information was provided in the question and we just needed to find some hidden patterns in the tabulated peptide sequences. But it actually needed more than that and involved some wordplay. If you are interested in the answer, please feel free to ask me.

The other interesting aspect is that there was no obvious way to submit the answer at https://ncats.io/challenge. If you read the instruction carefully, POST actually refers to the HTTP POST protocol. So, we had to POST the answer to that URL.

After we answered this questions, we then needed to complete 6 tasks. I posted an interesting task below. The first task is to solve an algorithm problem. This task was probably designed to test the computer science skills of the applicants.

<span style="color: #0000ff;">The Biomedical Data Translator consumes a wide variety of data from many sources. To help standardize the data being consumed, we have specified a <em>Knowledge Beacon</em> application programming interface (API) that can be found <a href="https://github.com/NCATS-Tangerine/translator-knowledge-beacon/" target="#foa">here</a>. The goal of this task is to give the participant familiarity with bringing new APIs online.</span>

<span style="color: #0000ff;">Lothar Collatz&#8217;s <a href="https://en.wikipedia.org/wiki/Collatz_conjecture" target="#foa">conjecture</a> produces <a href="https://oeis.org/A006577" target="#foa">sequences</a> that start from a natural number and have the following pattern:</span>

  1. <span style="color: #0000ff;">If <em>n</em> is even, divide <em>n</em> by 2.</span>
  2. <span style="color: #0000ff;">If <em>n</em> is odd, multiply <em>n</em> by 3 and add 1.</span>

<span style="color: #0000ff;"><b>Collatz siblings</b> are numbers that have the same path length; e.g., numbers 3 and 20 are siblings because both have path length 8. (Note that <i>path length</i> as defined here is the cardinality of the Collatz sequence starting from a given position.) Provide an API that produces Collatz siblings for a given set of integers whose path length <i>P</i> is bounded by 1 < <i>P</i> ≤ 64; for example, 21 and 128 are the only Collatz siblings of the integer set {3, 20}.</span>

<span style="color: #0000ff;">Please follow the specification provided in this <a href="https://ncats.io/challenge/assets/resources/swagger.yaml">Swagger API</a> definition file for your API implementation.</span>

&nbsp;

We completed this challenge and submitted a concept letter to NCATS. I don&#8217;t know what outcome we will have for our submission. But I want to send kudos to this NCATS program for designing this innovative proposal selection mechanism. After completing these tasks, we had a much better understanding of the research program, the review panel can probably have a direct evaluation of the technical capabilities of the applicants, and this process probably reduced the number of non-responsive proposals in this competition. Although this mechanism probably wouldn&#8217;t work in general, I hope the other research programs can also do more experimentation and innovation with their proposal submission and review processes.