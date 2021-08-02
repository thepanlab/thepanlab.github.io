---
id: 717
title: A graph-theoretic approach for the separation of b and y ions in tandem mass spectra.
date: 2014-11-02T23:20:51+00:00
author: omicsbio
layout: revision
guid: https://www.omicsbio.org/2014/11/02/234-autosave-v1/
permalink: /2014/11/02/234-autosave-v1/
---
Yan, B., <span style="color: #0000ff;">Chongle Pan</span>, Olman, V. N., Hettich, R. L. & Xu, Y.

<span style="color: #ff0000;"><em>Bioinformatics</em> </span>**21**, 563-574, doi:10.1093/bioinformatics/bti044 (2005).   [Link to Article]

<!--more-->

**Abstract:** MOTIVATION: Ion-type identification is a fundamental problem in computational proteomics. Methods for accurate identification of ion types provide the basis for many mass spectrometry data interpretation problems, including (a) de novo sequencing, (b) identification of post-translational modifications and mutations and (c) validation of database search results. RESULTS: Here, we present a novel graph-theoretic approach for solving the problem of separating b ions from y ions in a set of tandem mass spectra. We represent each spectral peak as a node and consider two types of edges: type-1 edge connecting two peaks probably of the same ion types and type-2 edge connecting two peaks probably of different ion types. The problem of ion-separation is formulated and solved as a graph partition problem, which is to partition the graph into three subgraphs, representing b, y and others ions, respectively, through maximizing the total weight of type-1 edges while minimizing the total weight of type-2 edges within each partitioned subgraph. We have developed a dynamic programming algorithm for rigorously solving this graph partition problem and implemented it as a computer program PRIME (PaRtition of Ion types in tandem Mass spEctra). The tests on a large amount of simulated mass spectra and 19 sets of high-quality experimental Fourier transform ion cyclotron resonance tandem mass spectra indicate that an accuracy level of approximately 90% for the separation of b and y ions was achieved.