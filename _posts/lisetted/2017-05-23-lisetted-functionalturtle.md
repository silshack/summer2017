--- 
layout: post
author: lisetted
title: "Lisette's functional turtle"
---


Functional turtle
<iframe src="https://trinket.io/embed/python/b3c7de28c4" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

Original
<iframe src="https://trinket.io/embed/python/effd2a2ed2" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

Reflection:
I decided I wanted to use my banjo turtle, but have the user determine the number of banjos in the function call. I soon realized while writing the code that I would need a do/for loop and so I shelved this idea for a future session. Instead, I decided to have the function call the banjo location on the screen. After I got rid of all the excess code, I struggled with how to make the banjo neck at the correct angle to come out of the round part in a way that lined up with the circle and realized Tina must have been facing a different direction in my old code. The first successful technique I used was to have tina draw half the circle (180 degrees of it), draw back over that half to where she started, and then draw the other half of the circle. This put her at the right position after drawing the circile. After some trial and error (and finding info on the position function here https://docs.python.org/2/library/turtle.html) I figured out I could also use the position function to my advantage. This meant that I could also have the function fall for the banjo tilt in addition to the location.
