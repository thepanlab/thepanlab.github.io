---
id: 286
title: 'Omega: an Overlap-graph de novo Assembler for Metagenomics.'
date: 2014-06-19T20:48:53+00:00
author: omicsbio
layout: default
parent: 2014 posts
grand_parent: Posts
---
<span style="color: #0000ff;">Bahlul Haider</span>, <span style="color: #0000ff;">Tae-Hyuk Ahn</span>, Bushnell, B., <span style="color: #0000ff;">Juanjuan Chai</span>, Copeland, A. & <span style="color: #0000ff;">Chongle Pan</span>

<span style="color: #ff0000;"><em>Bioinformatics</em></span>, 30(19):2717-22, doi:10.1093/bioinformatics/btu395 (2014). [[Link to Article](http://bioinformatics.oxfordjournals.org/content/30/19/2717)]

<!--more-->

**Abstract:** MOTIVATION: Metagenomic sequencing allows reconstruction of microbial genomes directly from environmental samples. Omega (overlap-graph metagenome assembler) was developed for assembling and scaffolding Illumina sequencing data of microbial communities. RESULTS: Omega found overlaps between reads using a prefix/suffix hash table. The overlap graph of reads was simplified by removing transitive edges and trimming short branches. Unitigs were generated based on minimum-cost flow analysis of the overlap graph and then merged to contigs and scaffolds using mate-pair information. In comparison to three de Bruijn graph assemblers (SOAPdenovo, IDBA-UD, and MetaVelvet), Omega provided comparable overall performance on a HiSeq 100-bp dataset and superior performance on a MiSeq 300-bp dataset. In comparison to Celera on the MiSeq dataset, Omega provided more continuous assemblies overall using a fraction of the computing time of existing Overlap-Layout-Consensus assemblers. This indicates Omega can more efficiently assemble longer Illumina reads, and at deeper coverage, for metagenomic datasets. Availability and Implementation: Implemented in C++ with source code and binaries freely available at [http://omega.omicsbio.org](http://omega.omicsbio.org/). CONTACT: panc@ornl.gov.

<p class="gde-text">
  <a href="https://www.omicsbio.org/wp-content/uploads/2014/06/Paper_2014_Haider_Omega_Assembler.pdf" class="gde-link" onClick="_gaq.push(['_trackEvent', 'Google Doc Embedder', 'Download', this.href]);">Download (PDF, Paper_2014_Haider_Omega_Assembler.pdf)</a>
</p>