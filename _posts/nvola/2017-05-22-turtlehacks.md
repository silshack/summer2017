---
layout: post
author: nvola
title: "Natasha's Turtlehack"
---
Here is my Turtlehack trinket. It requests a user's input for a color and a shape and creates a spiral pattern based on their input.

<iframe src="https://trinket.io/embed/python/b169535972?start=result" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>



I got the idea from this based on the Turtle Basics assignment; I really like the idea of loops and like the way that spirals look, so I thought it would be cool to not only figure out how to code loops to build spirals but to also incorporate some user input so that the user could personalize this a bit. 


The first thing I coded was the user input aspect; the Chapter 2 reading and exercises made this part very straightforward and easy to adapt to what I wanted to do. One thing that I found challenging was creating the loops (reasonably so, given that we haven't yet covered that topic). The first reading material I came across after looking online for loops in Python suggested using WHILE statements. These were pretty easy to figure out, and having taken some coding courses in the past I have a vague knowledge of how loops work so it wasn't difficult for me to figure out. What was difficult was dealing with the syntax; the material I found online did not explicitly explain that the WHILE statement required a colon so when I forgot to include the colon it was a little confusing about what was causing the error. I am also still a little unclear about the difference between FOR and WHILE loops, which I'm sure we'll get to soon. What took me the most time in creating these loops was more aesthetic than technical: figuring out how many iterations per size, what the base size should be, what the increase in size each iteration should be, etc.


Another issue I came across was writing the IF/ELSE IF statements, largely because I did not realize that in Python the ELSE IF function is called upon using "ELIF" (a handy abbreviation now that I know it). Again, I think I ran into errors remembering that the final ELSE statement requires a colon. 

```
if (user_shape == 'circle'):
  print('Building your ' + user_color + " circle pattern.")
  c_spirals()
elif (user_shape == 'square'):
  print('Building your ' + user_color + " square pattern.")
  s_spirals()
elif (user_shape == 'triangle'):
  print('Building your ' + user_color + " triangle pattern.")
  t_spirals()
else:
  print("You did not enter a valid shape. You get nothing.")
```


Another factor that made this assignment challenging for me was that I wanted to keep the code as clean as possible (at least for the ELSE IF statements, see above), so after some Googling I decided that I wanted to define each type of spiral as a function. This was a bit difficult to figure out because the reading I found online wasn't clear about what exactly constitutes the arguments when you're defining a function (I think I was even looking at Python documentation so that was pretty frustrating). Eventually I realized that these arguments were entirely optional and I was able to define functions for each type of spiral. See below:

```
def c_spirals():
 size = 20
 while size <200:
  iteration = 1
  while iteration < 7:
    tina.circle(size)
    tina.left(60)
    iteration = iteration +1
  size= size + 10
```

Lastly, I really wanted to incorporate a way to have the user select the origin for the spiral by clicking on the screen, however, after numerous attempts I couldn't get it to work (despite testing the method I was using in some test code, which worked).
