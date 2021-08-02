---
id: 641
title: 'MIDAS: A Database-Searching Algorithm for Metabolite Identification in Metabolomics.'
date: 2014-11-02T22:15:32+00:00
author: omicsbio
layout: revision
guid: https://www.omicsbio.org/2014/11/02/296-revision-v1/
permalink: /2014/11/02/296-revision-v1/
---
<span style="color: #0000ff;">Yingfeng Wang</span>, Kora, G., Bowen, B. P. & <span style="color: #0000ff;">Chongle Pan</span>

<span style="color: #ff0000;"><em>Analytical chemistry</em></span>, **86**, 9496-9503, doi:10.1021/ac5014783 (2014). [[Link to Article](http://pubs.acs.org/doi/abs/10.1021/ac5014783)]

<!--more-->

**[<img class="alignright wp-image-355 size-large" src="https://www.omicsbio.org/wp-content/uploads/2014/08/f1_v7_v2_small-1024x839.png" alt="f1_v7_v2_small" width="474" height="388" srcset="https://www.omicsbio.org/wp-content/uploads/2014/08/f1_v7_v2_small-1024x839.png 1024w, https://www.omicsbio.org/wp-content/uploads/2014/08/f1_v7_v2_small-300x246.png 300w, https://www.omicsbio.org/wp-content/uploads/2014/08/f1_v7_v2_small.png 1218w" sizes="(max-width: 474px) 100vw, 474px" />](https://www.omicsbio.org/wp-content/uploads/2014/08/f1_v7_v2_small.png)Abstract:** A database searching approach can be used for metabolite identification in metabolomics by matching the measured tandem mass spectra (MS/MS) against the predicted fragments of metabolites in a database. Here we present the open-source MIDAS algorithm (Metabolite Identification via Database Searching). To evaluate a metabolite-spectrum match (MSM), MIDAS first enumerates possible fragments from a metabolite by systematic bond dissociation, then calculates the plausibility of the fragments based on their fragmentation pathways, and finally scores the MSM to assess how well the experimental MS/MS spectrum from collision-induced dissociation (CID) is explained by the metabolite&#8217;s predicted CID MS/MS spectrum. MIDAS was designed to search high-resolution tandem mass spectra acquired on time-of-flight or Orbitrap mass spectrometer against a metabolite database in an automated and high-throughput manner. The accuracy of metabolite identification by MIDAS was benchmarked using four sets of standard tandem mass spectra from MassBank. On average, for 77% of original spectra and 84% of composite spectra, MIDAS correctly ranked the true compounds as the first MSMs out of all MetaCyc metabolites as decoys. MIDAS correctly identified 46% more original spectra and 59% more composite spectra at the first MSMs than an existing database-searching algorithm, MetFrag. MIDAS was showcased by searching a published real-world measurement of a metabolome from Synechococcus sp. PCC 7002 against the MetaCyc metabolite database. MIDAS identified many metabolites missed in the previous study. MIDAS identifications should be considered only as candidate metabolites, which need to be confirmed using standard compounds. To facilitate manual validation, MIDAS provides annotated spectra for MSMs and labels observed mass spectral peaks with predicted fragments. The database searching and manual validation can be performed online at [http://midas.omicsbio.org](http://midas.omicsbio.org/).

<p class="gde-text">
  <a href="https://www.omicsbio.org/wp-content/uploads/2014/08/Paper_2014_Wang_MIDAS_metabolomics.pdf" class="gde-link" onClick="_gaq.push(['_trackEvent', 'Google Doc Embedder', 'Download', this.href]);">Download (PDF, Paper_2014_Wang_MIDAS_metabolomics.pdf)</a>
</p>