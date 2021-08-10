---
layout: default
title: Development of an automated, adaptive, and scalable workflow for genome-resolved comparative metagenomics
date: 2016-11-30T22:46:10+00:00
author: omicsbio
parent: 2016 posts
grand_parent: Posts
---
# Development of an automated, adaptive, and scalable workflow for genome-resolved comparative metagenomics

In collaboration with Prof. Jill Banfield at UC Berkeley, we submitted a proposal to the JGI ETOP program. It was rejected.

&nbsp;

**Introduction**:

The growth in sequencing capacity of JGI has enabled analysis of many samples from an ecosystem, and sample numbers are likely to increase dramatically. We envision a time in the near future when researchers will want to analyze large study systems frequently and with high spatial resolution. This will allow, for example, contouring the distribution of microbial communities and their associated metabolic potential over ecological niches and tracking over time.  Automated data processing based on high-performance computing will be essential to meet this challenge.

** **

**Specific Aim 1: Construction and automation of an adaptive workflow** 

We have made significant progress in assembly of individual microbial genomes, reconstruction of their molecular functional profiles, and analysis of community taxonomical composition from large-scale comparative metagenomic studies. However, each step is typically handled separately, with significant user input, and computational demands currently make application of these approaches to large sample sets very challenging. Organizing the steps into a single workflow that can take advantage of high-performance computing should enable application of genome-resolved metagenomics at the ecosystem scale.

Our prior ETOP-funded work has provided considerable guidance as to how such a workflow should be constructed. Working across many biological systems, ranging from low-complexity consortia (e.g., simple enrichments) to highly diverse communities (e.g., soil), we have found that different methods work often best for different projects and even for recovery of certain genomes from a single project. Further, different methods are better optimized for different data types. For example, a de Bruijn graph-based assembler is more suitable for Illumina reads 100 bp long, whereas an overlap graph-based assembler performs better for Illumina data with >250 bp reads or for hybrid sequencing data with additional long reads. Similarly, binning algorithms based on tetranucleutide frequency may work accurately for simple communities with a few distinct lineages whereas more complex binning algorithms based on series sampling are typically essential for complex communities. Given the high diversity of metagenomics projects supported by JGI, it is essential to build an adaptive workflow that can choose the optimum algorithm from an array of options based on the community complexity, sequencing technology, and sampling strategies.

We propose to fully automate a workflow to meet the requirement of high throughput genome-resolved metagenomics at the JGI. Instead of a simple linear pipeline consisting of a fixed algorithm with pre-set parameters for each step, we will develop an automated adaptive workflow that incorporates rule-based decision trees to automatically choose algorithms and parameters based on input data and intermediate results. The workflow will be modular to enable incorporation of newly developed tools that arise from the broadest research community (e.g., new binning algorithms). This workflow will include the following steps: (1) sequencing data preprocessing; (2) metagenome assembly; (3) organism binning and taxonomy assignment; and (4) functional annotation. JGI users without prior experience in metagenomics will be able to directly use these results for biological analyses and advanced users can use the results to further optimize and re-run selected modules of this workflow.

** **

**Specific Aim 2: Scaling-up of computing-intensive tasks to the Cori supercomputer**

The metagenomics workflow contains many computing-intensive tasks. The read mapping tasks align short reads onto genomic sequences using tools such as Bowtie and BWA. The homology search tasks identify homologous sequences of a query gene or protein from a sequence database in NCBI and UniProt using methods such as BLAST or DIAMOND. The protein family search tasks find which protein family a query protein belongs to in Pfam, TIGRFam, UniFam, or other protein family databases using algorithms such as HMMER or RPS-BLAST.  The algorithms used in these tasks are not scaled up for supercomputers. This will become a bottleneck in processing large amounts of metagenomics data. Here, we will scale up these computationally expensive algorithms to the Cori supercomputer at NERSC. This will allow the proposed workflow to meet the exscientific needs of the user community.

We propose to scale up read mapping tasks, homology search tasks, and protein family search tasks to Cori. We will design a HPC computational framework to distribute the computation of these tasks across many compute nodes and perform load balancing and fault tolerance/recovery. The computation on individual Cori nodes will be performed by instances of a third-party algorithm. We will not develop new algorithms for these tasks; instead, we will enable our HPC framework to use existing algorithms and parallelize their processing over large datasets. As our benchmarking has indicated that the scalability bottleneck of these tasks is often data I/O, we will particularly optimize the I/O operations of the proposed HPC framework using Cori’s new Burst Buffer architecture. The input data for individual compute nodes will be staged on Burst Buffer and the output data will be stored or _in situ_ processed on Burst Buffer. In collaboration with the community at large, we will port existing algorithms to Intel Xeon Phi or use new algorithms designed specifically for Xeon Phi.

&nbsp;

**Specific Aim 3**: **Comparative analysis of genome-resolved metagenomics results**

One of the challenges that will be faced by researchers that generate very large numbers of metagenomic datasets for their study system will be to identify patterns in their data. To enable effective use of large sets of genomes obtained from many samples and linked abundance pattern and functional information, we will develop a suite of tools for comparative analysis. These tools will enable users to identify, for example, correlated organism abundance patterns (highlighting potential host-symbiont associations and other metabolic interdependencies) and links between organism abundances and geochemical conditions (possibly better connecting organisms to biogeochemical roles).

To achieve this goal, we will establish methods that can track specific genotypes across potentially hundreds or thousands of samples. This will require two steps (1) a redundancy reduction step in which genomes are classified as the same or different based on a user-defined threshold; and (2) tracking of organism abundances via read mapping (a step that will require computation on a supercomputer). Overall, the analysis tools will enable biologists to create functional/taxonomic profiles of ecosystems and to follow changes in composition and function with changing environmental conditions.