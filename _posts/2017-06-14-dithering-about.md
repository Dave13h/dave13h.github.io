---
layout: post
title: "Dithering About"
date: 2017-06-14
---
The great graphics lie continues! You put all this effort into rendering stuff in high dynamic range, funky tonemapping, fancy bloom effects and all that jazz and when it comes down to it, you have to smash all that quality into a 8-bit per component image for your monitor to display. The real victim of this bit-depth massacre is our poor flat shaded gradients, just look at that horrible banding -

<img src="/images/dithering_off.png" title="ew" />

Turns out, just like everything else in graphics rendering, you can cheat! Also turns out that dithering is still a thing :P

<img src="/images/dithering_on.png" title="hey, that's pretty good!" />

By appling just a smidge of noise to each pixel after your gamma correction can work wonders. 
