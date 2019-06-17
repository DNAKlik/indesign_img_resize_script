# indesign_scrip
Indesign script resize images from XML code and apply objectstyle based on XML

//figure_frame.jsx  
//Author: Walter Mulder - DNAklik
  
/** 
* @@@BUILDINFO@@@ figure_frame.jsx ! Version!  June 17 2019. 
* This script is an extension off FitAnchorToColumn v3 by Vinny
*/
//FitAnchorToColumn v3 
//Transform anchored objects in order to rescale them to make them fit column width, keeping proportions. 
//by Vinny 
/** 
* This script places  images referenced by impoted XML into object styles based on the XML code
* Images are rescaled with the code from FitAnchorToColumn v3
* The standaard maximum width is the width of the text column, but it can be overwritten if the width is assigned in the XML
* The figure element with figcaption is placed in a surounding Textframe
* A check is made to avoid changes to already processed images, for if the XML is relouded or updated by the link
* Check the information on https://github.com/DNAKlik/indesign_scrip and www.dnaklik.nl
 */
 
Example XML code
Outline image with caption:
<figure aid:pstyle="figure"><img href="file:///images/cart_part1.png" class="img-responsive"/> 
<figcaption aid:pstyle="figcaption">Voorbeeld van een outline image</figcaption></figure> 
Inline image with caption, two images next to each other:
<p aid:pstyle="p"><fig type="inline"><img href="file:///images/dna-plastiek-koe.png" width="310"/> 
<figcaption aid:pstyle="figcaption">Match DNA profile with a cow</figcaption></fig><fig type="inline"><img href="file:///images/dna-mondriaan-bloeiende-boom.png" width="310"/> 
<figcaption aid:pstyle="figcaption">Match DNA profile with a painting</figcaption></fig></p>
Inline image, surrounded by text:
<p aid:pstyle="p"><img-left type="inline"><img href="file:///images/avatar.png" width="100" height="100"/></img-left>This script is developed by Walter Mulder from DNAklik.</p>
Images equations (outline):
<math aid:pstyle="math"><img href="file:///math/bd751d42e38da75004bf2b0763fcd45c5b9706a0.144.000000.ffffff.1.png"/></math>
Images symbols (inline)
<p aid:pstyle="p">Dit symbool is <symbol aid:cstyle="symbol"><img href="file:///symbol/ddd3f0e090a89c5599901051a8f8c3b3c21f5317.144.000000.ffffff.1.png"/></symbol> die in de vergelijking staat</p> 
