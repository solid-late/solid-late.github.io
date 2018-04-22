---
layout: post
title:  "Problem with the prototype manufacturing and further ideas for the design"
date:   2018-04-22
category: 3dmodel
authors: julia
---
## Problem with the prototype manufacturing

This week we wanted to produce the prototype but a problem occurred so we were not able to do it.
The *pdf* file which contains the sketch for the laser cutting machine had incorrect dimensions: the
sketch in the pdf was approximately ten times bigger than the original sketch. The reason of this 
issue might be the fact that the *pdf* file was not generated directly by the **Fusion 360** software. 
The software has only offered to export the sketch as a *dxf* file, and there were no other options 
to convert it to *pdf*, so we used an [online file converter](https://www.zamzar.com/convert/dxf-to-pdf/) 
which created a pdf from the *dxf* file. Later we noticed that the dimensions of the generated file are 
incorrect so we tried another [online file converter](https://convertio.co/dxf-pdf/) and it also gave 
us an inappropriate result: this time the size of the sketch was correct, but the sketch was cropped.

![Sketch example](/static/img/3dmodel/incorrect_sketch.PNG)

Because of these problems it is more appropriate to find a way to create the *pdf* files directly. 

## Further ideas for the design

Also, some other points have to considered related to the 3D model. The place of the light sensor was
not discussed before. As the LED components are going to be on the surface of the front panel, it makes
sense to put the light sensor there too. Also the geometry should fit the micro servo motor which has
the following dimensions: 23 x 12.3 x 25.6 mm. As the final product is going to be assembled from wooden
sheets we have to know the exact thickness of them. The geometry contains some curved parts as well, they
are going to be created by the bending of laser cutted sheets. We need to get some further information how
to cut the sheets the way that they can be bended correctly.
