--- 
layout: post
author: nurahill
title: "Nura's Treasure Hunt Turtle"
---
Here is a link to the code:
<iframe src="https://trinket.io/embed/python/e9bc454a06" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

So, this one was hard for me. I am disapointed that I did not complete it. I was able to create a scenario for the game, meaning that I was able to design in. I ran out of time, so i did not really had functions to make it into a game. I feel like if i had one or two more hours, I could have done it. I was able use part of my original turtle drawing and use it as a design. I added rocks to the ground, which is where i did use a function:
```
#ROCKS
def rock(x,y):
  tina.penup()
  tina.goto(x,y)
  tina.pendown()
  tina.fill(True)
  tina.color("gray") #change this to light blue
  tina.circle(10)
  tina.fill(False)
  tina.pendown()
  tina.color("black")

rock(110,-155)
rock(155,-175)
rock(-180,-175)
rock(-150,-160)
rock(-120,-170)
rock(-80,-165)
rock(-50, -158)
rock(0,-170)
rock(30,-160)
rock(60,-170)
```
What i want to happen is for the user to find the turtles 'friend' (which is basically another turtle) under one of the rocks. The user shoud do that by putting in coordinates. I wasnt the turtle to move and change colors to indicate whether its close to its friend or not.
