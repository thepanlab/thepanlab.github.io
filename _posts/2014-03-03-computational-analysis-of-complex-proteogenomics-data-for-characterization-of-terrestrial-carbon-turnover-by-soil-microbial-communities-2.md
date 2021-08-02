---
id: 1007
title: Computational Analysis of Complex Proteogenomics Data for Characterization of Terrestrial Carbon Turnover by Soil Microbial Communities
date: 2014-03-03T16:33:59+00:00
author: Chongle Pan
layout: post
guid: https://www.omicsbio.org/?p=1007
permalink: /2014/03/03/computational-analysis-of-complex-proteogenomics-data-for-characterization-of-terrestrial-carbon-turnover-by-soil-microbial-communities-2/
categories:
  - Proposals
---
We were awarded 25 million CPU hours on the Titan supercomputer in the DOE ASCR ALCC user program.

**Summary**

Thanks for the development of next-generation sequencing and high-resolution mass spectrometry, proteogenomics has become a key data-driven technology for characterization of microbial communities in natural environments. We pioneered novel proteogenomics methodologies that used scalable data analytics algorithms and high-performance computing to generate new insights to complex microbial communities. We developed the Sipros algorithm and deployed it on Titan to identify proteins and their post-translation modifications using shotgun proteomics and to track the incorporation of labeled substrates into microbial populations using proteomic stable isotope probing. We developed a high-throughput genome functional annotation workflow using the new UniFam database and scaled taxonomic classification to large microbial communities using the Sigma algorithm on Titan. The scientific values and the computational scalability of these applications have been demonstrated on pilot small-scale studies on Titan.

Here we apply for computing resources on Titan to scale up these proteogenomics analyses to extremely complex soil communities in a model grassland ecosystem located in the Angelo reserve. The primary objective of this research is to determine which organisms, and by what processes, organic carbon is metabolized in deeper soil and the extent to which these are resilient to changes in climate associated with altered rainfall inputs. Community proteomics will be used to compare a manipulated rainfall regime representing future climates with a control regime. Proteomic stable isotope probing will be used to trace <sup>15</sup>N-, <sup>2</sup>H-, and <sup>13</sup>C-labeled substrates to the communities under different conditions. We will also compare metagenomes sequenced from a range of soil environments. Integration of these results will for the first time provide an organism-resolved molecular-level view of soil carbon cycling by microbial communities. To take advantage of the recent GPU upgrade on Titan, we will re-design Sipros and Sigma with GPU acceleration. The methods and algorithms developed in this study will be broadly applicable for analyses of complex ecosystems.

The proposed work on sample measurements and algorithm development has been funded by DOE Office of Biological and Environmental Research (BER). This directly supports DOE missions in characterization of terrestrial carbon cycling and modeling of climate changes. The requested allocation on Titan will enable and accelerate the analyses of large proteogenomics data and extract valuable biological information that cannot be recovered without leadership computing. The developed algorithms will be broadly useful and freely available to the proteogenomics community. Our work will enable more applications of computing-intensive proteogenomics for environmental microbiology studies of other ecosystems.