---
id: 927
title: Protocol for shotgun proteomics (MudPIT)
date: 2017-09-28T16:13:52+00:00
author: omicsbio
layout: revision
guid: https://www.omicsbio.org/2017/09/28/878-revision-v1/
permalink: /2017/09/28/878-revision-v1/
---
&nbsp;

This protocol was based on the original MudPIT protocol from the Yates lab. It was refined over the years at ORNL by Nathan VerBerkmoes, <span class="st">Melissa Thompson, Hayes McDonald, Rich Giannone, Paul Abraham, Greg Hurst, Bob Hettich, Zhou Li, and many other people at ORNL.</span>

&nbsp;

### <span style="text-decoration: underline;">Packing a Back Column</span>

#### Equipment used:

  1. Pressure Cell (New Objective)
  2. 150mm (ID) x 360mm (OD) Fused silica (Polymicro Technologies)
  3. Filter
  4. Union
  5. Ferrule x2
  6. SCX
  7. Aqua C-18

#### Procedure:

[<img class="wp-image-910 aligncenter" src="https://www.omicsbio.org/wp-content/uploads/2015/04/Picture1-300x59.png" alt="" width="631" height="124" srcset="https://www.omicsbio.org/wp-content/uploads/2015/04/Picture1-300x59.png 300w, https://www.omicsbio.org/wp-content/uploads/2015/04/Picture1-768x150.png 768w, https://www.omicsbio.org/wp-content/uploads/2015/04/Picture1-1024x200.png 1024w, https://www.omicsbio.org/wp-content/uploads/2015/04/Picture1-604x118.png 604w, https://www.omicsbio.org/wp-content/uploads/2015/04/Picture1.png 1456w" sizes="(max-width: 631px) 100vw, 631px" />](https://www.omicsbio.org/wp-content/uploads/2015/04/Picture1.png)

  1. Assemble column and union as shown above
  2. Check if union and filter are flowing well with MeOH (sonicate union with MeOH between runs).
  3. Make a slurry of SCX material by mixing SCX material with MeOH and vortexing for ~15 sec.
  4. Quickly place SCX material in pressure cell, insert column and pack until column reaches 1.5-2 cm.
  5. Chase with MeOH &#8211; remaining packing material should condense to a final column length of ~3 cm. Repeat steps 4 and 5 if column is not long enough.
  6. Make a slurry of C18 RP material by mixing C18 RP material with MeOH. Material will quickly fall out of solution.
  7. Place C18 in pressure cell and insert column above level of packing material.
  8. Turn on gas and bounce the column 1-2 times from the bottom of the tube to above the packing material.  The final position should be above the packing material.  Wait for the material to condense.
  9. Repeat step 8 until column reaches ~3 cm.
 10. Chase with Solvent A (95% H<sub>2</sub>O, 5%ACN, 0.1% F.A.) for 10 min. to equilibrate column.

&nbsp;

### <span style="text-decoration: underline;">Packing a Front Column</span>

#### Equipment used:

  1. Pressure Cell
  2. 100mm (ID) x 360mm (OD) Fused silica
  3. A PicoTip column from New Objective
  4. Aqua C-18

#### Procedure:

  1. Cut column to ~25-30cm.
  2. Mix C-18 slurry.  Material will quickly fall out of solution.
  3. Place C-18 in pressure cell and insert column above level of packing material.
  4. Turn on gas and bounce the column 1-2 times from the bottom of the tube to above the packing material.  The final position should be above the packing material.  Wait for the material to condense.
  5. Repeat step 4 until column reaches ~15 cm.
  6. Finish “packing” column on HPLC pump at a flow rate of 200-500nL/min with 100% Solvent B (30% H<sub>2</sub>O, 70% ACN, 0.1% F.A.) then equilibrate back to 100% Solvent A (95% H<sub>2</sub>O, 5% ACN, 0.1% F.A.) for 10 min. to condition column.
  7. Cut column to ~20 cm.

&nbsp;

### <u>Back column wash to move peptides from RP to SCX </u>

Flow rates depend on pump and split method, flow rates are an approximate below.

<table width="623">
  <tr>
    <td width="148">
      <strong>Time (min)</strong>
    </td>
    
    <td width="187">
      <strong>Flow (nl/min)</strong>
    </td>
    
    <td width="72">
      <strong>%A</strong>
    </td>
    
    <td width="72">
      <strong>%B</strong>
    </td>
    
    <td width="72">
      <strong>%C</strong>
    </td>
    
    <td width="72">
      <strong>%D</strong>
    </td>
  </tr>
  
  <tr>
    <td width="148">
    </td>
    
    <td width="187">
      600
    </td>
    
    <td width="72">
      100
    </td>
    
    <td width="72">
    </td>
    
    <td width="72">
    </td>
    
    <td width="72">
    </td>
  </tr>
  
  <tr>
    <td width="148">
      15
    </td>
    
    <td width="187">
      600
    </td>
    
    <td width="72">
      100
    </td>
    
    <td width="72">
    </td>
    
    <td width="72">
    </td>
    
    <td width="72">
    </td>
  </tr>
  
  <tr>
    <td width="148">
      20
    </td>
    
    <td width="187">
      600
    </td>
    
    <td width="72">
    </td>
    
    <td width="72">
      100
    </td>
    
    <td width="72">
    </td>
    
    <td width="72">
    </td>
  </tr>
  
  <tr>
    <td width="148">
      25
    </td>
    
    <td width="187">
      600
    </td>
    
    <td width="72">
      100
    </td>
    
    <td width="72">
    </td>
    
    <td width="72">
    </td>
    
    <td width="72">
    </td>
  </tr>
  
  <tr>
    <td width="148">
      30
    </td>
    
    <td width="187">
      600
    </td>
    
    <td width="72">
    </td>
    
    <td width="72">
      100
    </td>
    
    <td width="72">
    </td>
    
    <td width="72">
    </td>
  </tr>
  
  <tr>
    <td width="148">
      35
    </td>
    
    <td width="187">
      600
    </td>
    
    <td width="72">
      100
    </td>
    
    <td width="72">
    </td>
    
    <td width="72">
    </td>
    
    <td width="72">
    </td>
  </tr>
  
  <tr>
    <td width="148">
      40
    </td>
    
    <td width="187">
      600
    </td>
    
    <td width="72">
    </td>
    
    <td width="72">
      100
    </td>
    
    <td width="72">
    </td>
    
    <td width="72">
    </td>
  </tr>
  
  <tr>
    <td width="148">
      45
    </td>
    
    <td width="187">
      600
    </td>
    
    <td width="72">
      100
    </td>
    
    <td width="72">
    </td>
    
    <td width="72">
    </td>
    
    <td width="72">
    </td>
  </tr>
</table>

&nbsp;

&nbsp;

### <u>2D Gradients</u>

Flow rates depend on pump and split method, flow rates are an approximate below, measured at tip of nanospray.

&nbsp;

Step 1

<table width="519">
  <tr>
    <td style="width: 113.317px;">
      <strong>Time (min)</strong>
    </td>
    
    <td style="width: 144.95px;">
      <strong>Flow (nl/min)</strong>
    </td>
    
    <td style="width: 56px;">
      <strong>%A</strong>
    </td>
    
    <td style="width: 55.7833px;">
      <strong>%B</strong>
    </td>
    
    <td style="width: 55.75px;">
      <strong>%C</strong>
    </td>
    
    <td style="width: 56px;">
      <strong>%D</strong>
    </td>
  </tr>
  
  <tr>
    <td style="width: 113.317px;">
    </td>
    
    <td style="width: 144.95px;">
      300
    </td>
    
    <td style="width: 56px;">
      100
    </td>
    
    <td style="width: 55.7833px;">
    </td>
    
    <td style="width: 55.75px;">
    </td>
    
    <td style="width: 56px;">
    </td>
  </tr>
  
  <tr>
    <td style="width: 113.317px;">
      5
    </td>
    
    <td style="width: 144.95px;">
      300
    </td>
    
    <td style="width: 56px;">
      100
    </td>
    
    <td style="width: 55.7833px;">
    </td>
    
    <td style="width: 55.75px;">
    </td>
    
    <td style="width: 56px;">
    </td>
  </tr>
  
  <tr>
    <td style="width: 113.317px;">
      5.01
    </td>
    
    <td style="width: 144.95px;">
      600
    </td>
    
    <td style="width: 56px;">
      95
    </td>
    
    <td style="width: 55.7833px;">
    </td>
    
    <td style="width: 55.75px;">
    </td>
    
    <td style="width: 56px;">
      5
    </td>
  </tr>
  
  <tr>
    <td style="width: 113.317px;">
      7.5
    </td>
    
    <td style="width: 144.95px;">
      600
    </td>
    
    <td style="width: 56px;">
      95
    </td>
    
    <td style="width: 55.7833px;">
    </td>
    
    <td style="width: 55.75px;">
    </td>
    
    <td style="width: 56px;">
      5
    </td>
  </tr>
  
  <tr>
    <td style="width: 113.317px;">
      7.51
    </td>
    
    <td style="width: 144.95px;">
      600
    </td>
    
    <td style="width: 56px;">
      100
    </td>
    
    <td style="width: 55.7833px;">
    </td>
    
    <td style="width: 55.75px;">
    </td>
    
    <td style="width: 56px;">
    </td>
  </tr>
  
  <tr>
    <td style="width: 113.317px;">
      10
    </td>
    
    <td style="width: 144.95px;">
      600
    </td>
    
    <td style="width: 56px;">
      100
    </td>
    
    <td style="width: 55.7833px;">
    </td>
    
    <td style="width: 55.75px;">
    </td>
    
    <td style="width: 56px;">
    </td>
  </tr>
  
  <tr>
    <td style="width: 113.317px;">
      10.01
    </td>
    
    <td style="width: 144.95px;">
      300
    </td>
    
    <td style="width: 56px;">
      100
    </td>
    
    <td style="width: 55.7833px;">
    </td>
    
    <td style="width: 55.75px;">
    </td>
    
    <td style="width: 56px;">
    </td>
  </tr>
  
  <tr>
    <td style="width: 113.317px;">
      20
    </td>
    
    <td style="width: 144.95px;">
      300
    </td>
    
    <td style="width: 56px;">
      90
    </td>
    
    <td style="width: 55.7833px;">
      10
    </td>
    
    <td style="width: 55.75px;">
    </td>
    
    <td style="width: 56px;">
    </td>
  </tr>
  
  <tr>
    <td style="width: 113.317px;">
      120
    </td>
    
    <td style="width: 144.95px;">
      300
    </td>
    
    <td style="width: 56px;">
      50
    </td>
    
    <td style="width: 55.7833px;">
      50
    </td>
    
    <td style="width: 55.75px;">
    </td>
    
    <td style="width: 56px;">
    </td>
  </tr>
</table>

&nbsp;

Steps 2-10. Same set up as Step 1 varying only the % D as follows

This should be optimized for any given LC:

  * Step 2              7%
  * Step 3              10%
  * Step 4              12%
  * Step 5              15%
  * Step 6              17%
  * Step 7              20%
  * Step 8              25%
  * Step 9              35%
  * Step 10            50%

Step 11

<table style="height: 16px;" width="519">
  <tr style="height: 9px;">
    <td style="height: 9px; width: 113.317px;">
      <strong>Time (min)</strong>
    </td>
    
    <td style="height: 9px; width: 144.95px;">
      <strong>Flow (nl/min)</strong>
    </td>
    
    <td style="height: 9px; width: 56px;">
      <strong>%A</strong>
    </td>
    
    <td style="height: 9px; width: 55.7833px;">
      <strong>%B</strong>
    </td>
    
    <td style="height: 9px; width: 55.75px;">
      <strong>%C</strong>
    </td>
    
    <td style="height: 9px; width: 56px;">
      <strong>%D</strong>
    </td>
  </tr>
  
  <tr style="height: 5px;">
    <td style="height: 5px; width: 113.317px;">
    </td>
    
    <td style="height: 5px; width: 144.95px;">
      300
    </td>
    
    <td style="height: 5px; width: 56px;">
      100
    </td>
    
    <td style="height: 5px; width: 55.7833px;">
    </td>
    
    <td style="height: 5px; width: 55.75px;">
    </td>
    
    <td style="height: 5px; width: 56px;">
    </td>
  </tr>
  
  <tr style="height: 5px;">
    <td style="height: 5px; width: 113.317px;">
      5
    </td>
    
    <td style="height: 5px; width: 144.95px;">
      300
    </td>
    
    <td style="height: 5px; width: 56px;">
      100
    </td>
    
    <td style="height: 5px; width: 55.7833px;">
    </td>
    
    <td style="height: 5px; width: 55.75px;">
    </td>
    
    <td style="height: 5px; width: 56px;">
    </td>
  </tr>
  
  <tr style="height: 5px;">
    <td style="height: 5px; width: 113.317px;">
      5.01
    </td>
    
    <td style="height: 5px; width: 144.95px;">
      600
    </td>
    
    <td style="height: 5px; width: 56px;">
    </td>
    
    <td style="height: 5px; width: 55.7833px;">
    </td>
    
    <td style="height: 5px; width: 55.75px;">
    </td>
    
    <td style="height: 5px; width: 56px;">
      100
    </td>
  </tr>
  
  <tr style="height: 5px;">
    <td style="height: 5px; width: 113.317px;">
      10
    </td>
    
    <td style="height: 5px; width: 144.95px;">
      600
    </td>
    
    <td style="height: 5px; width: 56px;">
    </td>
    
    <td style="height: 5px; width: 55.7833px;">
    </td>
    
    <td style="height: 5px; width: 55.75px;">
    </td>
    
    <td style="height: 5px; width: 56px;">
      100
    </td>
  </tr>
  
  <tr style="height: 5px;">
    <td style="height: 5px; width: 113.317px;">
      10.01
    </td>
    
    <td style="height: 5px; width: 144.95px;">
      600
    </td>
    
    <td style="height: 5px; width: 56px;">
      100
    </td>
    
    <td style="height: 5px; width: 55.7833px;">
    </td>
    
    <td style="height: 5px; width: 55.75px;">
    </td>
    
    <td style="height: 5px; width: 56px;">
    </td>
  </tr>
  
  <tr style="height: 5px;">
    <td style="height: 5px; width: 113.317px;">
       15
    </td>
    
    <td style="height: 5px; width: 144.95px;">
      600
    </td>
    
    <td style="height: 5px; width: 56px;">
      100
    </td>
    
    <td style="height: 5px; width: 55.7833px;">
       0
    </td>
    
    <td style="height: 5px; width: 55.75px;">
    </td>
    
    <td style="height: 5px; width: 56px;">
    </td>
  </tr>
  
  <tr style="height: 5px;">
    <td style="height: 5px; width: 113.317px;">
      15.01
    </td>
    
    <td style="height: 5px; width: 144.95px;">
      300
    </td>
    
    <td style="height: 5px; width: 56px;">
      100
    </td>
    
    <td style="height: 5px; width: 55.7833px;">
    </td>
    
    <td style="height: 5px; width: 55.75px;">
    </td>
    
    <td style="height: 5px; width: 56px;">
    </td>
  </tr>
  
  <tr style="height: 5px;">
    <td style="height: 5px; width: 113.317px;">
      17
    </td>
    
    <td style="height: 5px; width: 144.95px;">
      300
    </td>
    
    <td style="height: 5px; width: 56px;">
      90
    </td>
    
    <td style="height: 5px; width: 55.7833px;">
      10
    </td>
    
    <td style="height: 5px; width: 55.75px;">
    </td>
    
    <td style="height: 5px; width: 56px;">
    </td>
  </tr>
  
  <tr style="height: 16px;">
    <td style="height: 16px; width: 113.317px;">
      120
    </td>
    
    <td style="height: 16px; width: 144.95px;">
      300
    </td>
    
    <td style="height: 16px; width: 56px;">
    </td>
    
    <td style="height: 16px; width: 55.7833px;">
      100
    </td>
    
    <td style="height: 16px; width: 55.75px;">
    </td>
    
    <td style="height: 16px; width: 56px;">
    </td>
  </tr>
</table>

### <u>2D Plumbing</u>

[<img class=" wp-image-883 aligncenter" src="https://www.omicsbio.org/wp-content/uploads/2017/09/MudPIT-plumbing-300x215.png" alt="" width="621" height="446" srcset="https://www.omicsbio.org/wp-content/uploads/2017/09/MudPIT-plumbing-300x215.png 300w, https://www.omicsbio.org/wp-content/uploads/2017/09/MudPIT-plumbing-378x270.png 378w" sizes="(max-width: 621px) 100vw, 621px" />](https://www.omicsbio.org/wp-content/uploads/2017/09/MudPIT-plumbing.png)

&nbsp;

### <u>Column and Gradient Theory.</u>

  1. Sample is loaded onto back column.  The majority of the peptides bind to C-18.  The remainder should bind to the SCX.
  2. Back column wash to move peptides from RP to SCX
  3. Attach back column to front column between HPLC and Mass Spec.
  4. Runs 1-11 (Salt Pulses followed by RP gradient): Peptides sequentially elute off of the SCX of the back column according to their ionic strength and bind to the front column and are separated by the RP gradient.

**<u> </u>**

### <u>Solvents and Solutions</u>

  * Solvent A: 95% H2O, 5% ACN, 0.1% F.A.
  * Solvent B: 30% H2O, 70% ACN, 0.1% F.A.
  * Solvent D: 500mM Ammonium Acetate: made in solvent A.  Should be pH 2.5 – no need to adjust.

All solvents from Burdick and Jackson

&nbsp;

### <span style="text-decoration: underline;">Parts and Materials</span>

<table width="711">
  <tr style="height: 22px;">
    <td style="height: 22px;" width="174">
      <strong>Item</strong>
    </td>
    
    <td style="height: 22px;" width="140">
      <strong>Vendor</strong>
    </td>
    
    <td style="height: 22px;" width="163">
      <strong>Description</strong>
    </td>
    
    <td style="height: 22px;" width="89">
      <strong>Part#</strong>
    </td>
    
    <td style="height: 22px;" width="145">
      <strong>Quantity/unit</strong>
    </td>
  </tr>
  
  <tr style="height: 22px;">
    <td style="height: 22px;" width="174">
      Pressure Cell
    </td>
    
    <td style="height: 22px;" width="140">
      New Objective
    </td>
    
    <td style="height: 22px;" width="163">
    </td>
    
    <td style="height: 22px;" width="89">
    </td>
    
    <td style="height: 22px;" width="145">
    </td>
  </tr>
  
  <tr style="height: 22px;">
    <td style="height: 22px;" width="174">
      Fused Silica
    </td>
    
    <td style="height: 22px;" width="140">
    </td>
    
    <td style="height: 22px;" width="163">
      150x360mm
    </td>
    
    <td style="height: 22px;" width="89">
    </td>
    
    <td style="height: 22px;" width="145">
    </td>
  </tr>
  
  <tr style="height: 22px;">
    <td style="height: 22px;" width="174">
      Fused Silica
    </td>
    
    <td style="height: 22px;" width="140">
    </td>
    
    <td style="height: 22px;" width="163">
      100x360mm
    </td>
    
    <td style="height: 22px;" width="89">
    </td>
    
    <td style="height: 22px;" width="145">
    </td>
  </tr>
  
  <tr style="height: 22px;">
    <td style="height: 22px;" width="174">
      Ferrules
    </td>
    
    <td style="height: 22px;" width="140">
      Upchurch
    </td>
    
    <td style="height: 22px;" width="163">
      Standard Head Fitting
    </td>
    
    <td style="height: 22px;" width="89">
      F-1245
    </td>
    
    <td style="height: 22px;" width="145">
    </td>
  </tr>
  
  <tr style="height: 22px;">
    <td style="height: 22px;" width="174">
      Filter
    </td>
    
    <td style="height: 22px;" width="140">
      Upchurch
    </td>
    
    <td style="height: 22px;" width="163">
      Filter End Fitting
    </td>
    
    <td style="height: 22px;" width="89">
      M-120x
    </td>
    
    <td style="height: 22px;" width="145">
      10/pack
    </td>
  </tr>
  
  <tr style="height: 67px;">
    <td style="height: 67px;" width="174">
      Union
    </td>
    
    <td style="height: 67px;" width="140">
      Upchurch
    </td>
    
    <td style="height: 67px;" width="163">
      Microfilter assembly, inline, 0.5um Peek, Microtight
    </td>
    
    <td style="height: 67px;" width="89">
      M-520
    </td>
    
    <td style="height: 67px;" width="145">
      5
    </td>
  </tr>
  
  <tr style="height: 22px;">
    <td style="height: 22px;" width="174">
      Luna 5u SCX
    </td>
    
    <td style="height: 22px;" width="140">
      Phenomenex
    </td>
    
    <td style="height: 22px;" width="163">
      100A
    </td>
    
    <td style="height: 22px;" width="89">
      04A-4398
    </td>
    
    <td style="height: 22px;" width="145">
    </td>
  </tr>
  
  <tr style="height: 22px;">
    <td style="height: 22px;" width="174">
      Aqua 64 C-18
    </td>
    
    <td style="height: 22px;" width="140">
      Phenomenex
    </td>
    
    <td style="height: 22px;" width="163">
      200A
    </td>
    
    <td style="height: 22px;" width="89">
    </td>
    
    <td style="height: 22px;" width="145">
    </td>
  </tr>
  
  <tr style="height: 22px;">
    <td style="height: 22px;" width="174">
      2ml tubes
    </td>
    
    <td style="height: 22px;" width="140">
    </td>
    
    <td style="height: 22px;" width="163">
    </td>
    
    <td style="height: 22px;" width="89">
    </td>
    
    <td style="height: 22px;" width="145">
    </td>
  </tr>
  
  <tr style="height: 22px;">
    <td style="height: 22px;" width="174">
      Picotip Emitter
    </td>
    
    <td style="height: 22px;" width="140">
      New Objective
    </td>
    
    <td style="height: 22px;" width="163">
      PF360-100-15-N-5
    </td>
    
    <td style="height: 22px;" width="89">
      PicoFrit
    </td>
    
    <td style="height: 22px;" width="145">
    </td>
  </tr>
  
  <tr style="height: 22px;">
    <td style="height: 22px;" width="174">
      Microferrule Plug
    </td>
    
    <td style="height: 22px;" width="140">
      Upchurch
    </td>
    
    <td style="height: 22px;" width="163">
    </td>
    
    <td style="height: 22px;" width="89">
      P-116
    </td>
    
    <td style="height: 22px;" width="145">
      5
    </td>
  </tr>
  
  <tr style="height: 44px;">
    <td style="height: 44px;" width="174">
      Microtee
    </td>
    
    <td style="height: 44px;" width="140">
      Upchurch
    </td>
    
    <td style="height: 44px;" width="163">
      Microtee for 360um tubing
    </td>
    
    <td style="height: 44px;" width="89">
      P-888
    </td>
    
    <td style="height: 44px;" width="145">
      5
    </td>
  </tr>
</table>

&nbsp;