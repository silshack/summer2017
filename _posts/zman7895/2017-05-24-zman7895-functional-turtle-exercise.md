---
layout: post
author: zman7895
title: "zman7895's Functional Turtle Exercise"
---
Below is my duplicated trinket with the functional updates followed by my original.
<iframe src="https://trinket.io/embed/python/97ff493544" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>
<iframe src="https://trinket.io/embed/python/ccad0f5a12" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>


Wowsers, I thought I had felt frustration before, but this was by far the most frustrated I have gotten working in this class. Part of that, is because I truly felt comfortable during the reading, in the sense I thought I was really getting it. However, once I started playing with my trinket I ran into so many issues, and a few I never figured out. The biggest problem I had was with my editTurtle function. It ultimately became just a function to take a turtle that had already been instantiated and simply editing its color and shape. But, what I wanted was for this function to create the turtle from scratch. No matter what I tried, it wouldn't work because it always said later in my code that the turtle I thought I was creating didn't exist. I tried multiple methods, including having an instantiation statement in my function, but it still felt like it never left the function. I even returned the turtle that was created, in hopes it would then be able to be used later on, but nothing happened. 
```
def createTurtle(name, shape, color):
  name = turtle.Turtle()
  name.shape(shape)
  name.color(color)
  return name
```
I thought this code would make it so the person could enter the name and have that create a new turtle, but this code didn't work, and neither did all my slight variations of this. I can't wait to figure out how to do this!


I did like the changing of my game over function. Rather than having the repetitive code of asking if the game had ended after every question, I now created a gameover function and simply called that one line after each question. I also liked adding the ability to turn the creation of the finish line into a function and be able to choose whatever color you want the finish line to be. Overall, while frustrated as hell with the createTurtle function, I am pleased with the addition and implementation of the other functions, and that felt good, which I needed!
