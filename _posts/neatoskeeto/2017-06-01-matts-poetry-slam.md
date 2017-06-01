---
layout: post
author: neatoskeeto
title: "Matt's poetry slam turtle"
---
<iframe src="https://trinket.io/embed/python/0a07661859" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

The first thing I wanted to do was to incorporate more randomness in the presentation, so I had the background color generate randomly using randint for the red green and blue values.
I next needed to make sure the text stayed within the box, so I moved the turtle to the top of the box at the beginning and had it move 20 pixels down to before writing a line. 
I set up a variable to track the turtle's x and y positions, and put an if statement that ends the program if the turtle goes below the bottom of the screen (y < -180). 
I figured out how to use a monospace font to make it easier to count the horizontal spaces. I spent some time trying to figure out how to make a loop that would divide lines that are too long into shorter lines, but I ran out of time.
The last thing I did was to add a compliment when the user finished, because those are always nice.
