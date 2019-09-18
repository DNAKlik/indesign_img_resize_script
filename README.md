# indesign script resize  images and apply object style from XML import
Indesign script resize images from XML code and apply objectstyle based on XML

// figure_frame.jsx  
// Author: Walter Mulder - DNAklik
// www.dnaklik.nl
  
/** 
* @@@BUILDINFO@@@ figure_frame.jsx ! Version!  June 21 2019. 
* This script is an extension off FitAnchorToColumn v8 by Vinny
*/
//FitAnchorToColumn v3 
//Transform anchored objects in order to rescale them to make them fit column width, keeping proportions. 
//by Vinny 
/** 
* This script places  images referenced by impoted XML into object styles based on the XML code
* Images are rescaled with the code from FitAnchorToColumn v8
* The standaard maximum width is the width of the text column, but it can be overwritten if the width is assigned in the XML
* The figure element with figcaption is placed in a surounding Textframe
* A check is made to avoid changes to already processed images, for if the XML is relouded or updated by the link
* Check the information on https://github.com/DNAKlik/indesign_scrip and www.dnaklik.nl
 */
 
Example XML code
Outline image with caption:
```xml
<figure aid:pstyle="figure"><img href="file:///images/cart_part1.png" class="img-responsive"/> 
<figcaption aid:pstyle="figcaption">Voorbeeld van een outline image</figcaption></figure>
```
Inline image with caption, two images next to each other:
```xml
<p aid:pstyle="p"><fig aid:cstyle="fig" type="inline"><img href="file:///images/dna-plastiek-koe.png" width="310"/> 
<figcaption aid:pstyle="figcaption">Match DNA profile with a cow</figcaption></fig><fig aid:cstyle="fig" type="inline"><img href="file:///images/dna-mondriaan-bloeiende-boom.png" width="310"/> 
<figcaption aid:pstyle="figcaption">Match DNA profile with a painting</figcaption></fig></p>
```
Inline image, surrounded by text:
```xml
<p aid:pstyle="p"><img-left aid:cstyle="img-left" type="inline"><img href="file:///images/avatar.png" width="100" height="100"/></img-left>This script is developed by Walter Mulder from DNAklik.</p>
```
Images equations (outline):
```xml
<math aid:pstyle="math"><Table aid:table="table" aid:trows="1" aid:tcols="2" aid5:tablestyle="equation"><Cell aid:table="cell" aid5:cellstyle="eq" aid:crows="1" aid:ccols="1" aid:ccolwidth="460.00"><eq><img href="file:///math/tex-57w2bC.pdf" width="144%"/></eq></Cell><Cell aid:table="cell" aid5:cellstyle="eq_nr" aid:crows="1" aid:ccols="1" aid:ccolwidth="60.00"><p_eq_nr aid:pstyle="p_eq_nr"/></Cell></Table></math>
```
Images symbols (inline)
```xml
<p aid:pstyle="p">Dit symbool is <symbol aid:cstyle="symbol"><img href="file:///symbol/tex-hDKnus.pdf" width="144%"/></symbol> die in de vergelijking staat</p>
```
