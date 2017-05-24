---
layout: post
author: jpanken
title: "Jaffa's Functional Turtle"
---

Original:

<iframe src="https://trinket.io/embed/python/4096f57634" width="100%" height="356" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>


Functional:


<iframe src="https://trinket.io/embed/python/cc4ce2bf3b" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

Remix:


<iframe src="https://trinket.io/embed/python/e6cf5bfae9" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>



I modified my first turtle because I thought that I could condense the code and make it a little more interesting.  The first thing I did was change the pattern of drawing the squares so that they all went to the left.  This was a lot more efficient.  It also allowed me to define draw_square using size as an argument instead of direction.  Then, I tried to incorporate a function with a return.  I imported the random module so that I could randomize the choice of colors.  It took me some time to figure out how to code the colors because the quotation marks were getting confusing.  Initially, I tried to use random.choice, but I couldn't get it to work so I switched to random.randint instead.  This allowed me to write an if-elif-else statement that translated the integers into colors.  


I wanted to incorporate the return function so that I could then print the color that was chosen.  Eventually, I figured out how to get it to generate the integer, but not the color.  However, the integer did not represent the color shown, but was just another random integer.  I never did figure out how to get that work, maybe another assignment?


I think that my choice to do the basic turtle was not as challenging as I thought it could be.  I think that the Functional Turtle is--at least--an improvement over the Basic Turtle, but definitely not groundbreaking.  So I made a remix of the Functional Turtles that uses a loop.  When I see what the other students in the class can do, I always feel discouraged because these things take me more time.  I'm trying not to get frustrated, but it's difficult.  Hopefully, things will click for me soon...
