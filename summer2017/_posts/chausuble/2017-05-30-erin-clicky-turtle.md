--- 
layout: post
author: chausuble
title: "Erin's Clicky Coloring Chicken Turtle"
---

<iframe src="https://trinket.io/embed/python/ef74681605" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

The exercises really exhausted me, and a bizarre glitch with Trinket made completing this pretty hard.

My turtle is a coloring page - you click on different body parts on the chicken, and it will fill in the color you type in.
I did this through having the turtle draw the chicken part by part during setup(), and then, when coloring it, it would first
retrace the body part you select, then use the fill() function to color it. Sounds simple enough...

But I'm telling you, something downright strange happened. The program was working fine for a while. Then, at one point, with me 
changing nothing, whenever it was time to color any body part, it would instead re-draw the body at whatever bizarre angle
I left it at. Nothing I did changed it! I could isolate each part in separate trinkets, and they would work fine. Once they
all came together, it broke. It got to the point where one version I made, I deleted every trace of the body drawing function...
and it STILL drew the body! I gave it up for the night. Then, of course, magically - I changed nothing at all - I woke up in
the morning and the program worked fine. I don't even know anymore...

So that adventure was long enough. Sleeping on it, however, did help me come up with solutions to little problems - issues like
how, at first, when you colored in the head, it would also color over the beak and eye. Having the colorhead() function redraw
the eye and beak resolved that. 

There are still some problems I simply don't have time to fix - for example, for some reason, the penup() in the body doesn't 
work completely, so after the body is colored in, you'll see a trace of the angle from where you clicked on the body. A 
similar problem sometimes happens to the head, too. This is probably a matter of where I have the penup() function. 
Furthermore, if you click on one body part, don't type in anything, and then click on another body part and type in a color, 
it will color in the first body part with that color, but not the second. I think this could be resolved through the while 
loop, but I can't think of how to do it right now.
