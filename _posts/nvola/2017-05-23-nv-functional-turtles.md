---
layout: post
author: nvola
title: "Natasha's Functional Turtles"
---
For my functional turtle exercise I decided to refactor what I submitted for the Turtle Basics assignment which essentially just created a spiral/nautilus pattern made from squares. The original is below:


<iframe src="https://trinket.io/embed/python/26c2de5c1d" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>


For the new code, I decided to incoporate user input and to create three functions. The first function is a loop to make the nautilus shape; the user input determines how many iterations for the loop and thus how many squares a drawn. The second functions returns the number of lines drawn as a result. The third function randomly generates a color and uses the output as the color for that iteration of the loop. See below:



<iframe src="https://trinket.io/embed/python/2e26879c5a" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>



I first started this by creating the loop to draw the shape based on the user input. The syntax of it was fairly straightforward and easy because I had used loops in previous assignments, however, try as I might, I could not get the loop to recreate the clean nautilus shape from the original, even when I had the angles set the same. The end product is okay aesthetically, and has different angles from those in the original, but I want to figure out what went wrong.



Then I created the function that counted the number of lines drawn by multiplying the user input by 4 (simple, I know, but I was in a time crunch!). This was pretty easy, since I'd spent the time doing the chapter exercises earlier.


Then I decided that I wanted some "flair," so I thought it would be cool to have the colors randomly change so that each time the program produced something slightly different. Thus, I created another function that randomly generated a color and incorporated that function as part of the loop that creates the pattern. Another way to do something similar (adding color) might have been to create a list of colors and to create a subloop in the pattern loop to loop through the list of colors, but the random color method I ended up using allowed me to import the random module and incorporate some of what I learned about lists doing the Logical Turtles exercises. 
