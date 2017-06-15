---
layout: post
author: Ibbi2010
title: "Ibbi2010's Class Hack"
---
Reflection:
The concept of Classes always boggled my mind and I knew I needed some serious reading. I spent good amount of time going through the recommeded readings. I understood the concept in theory but was not able to get he functionality of Custom Classes.I struggled with  the 'cats'and the'dogs'examples and got further confused. Finally I watched the videos which simplified things for me. I started thinking of ways to incorporate classes into my final project. For my Class Hack, I treated this assignment entirely to make myself more comfortabe with the idea of using and playing around with Class. 
Instead of constructing a new class from the scrtach I extended the built-in Turtle class in one of my previous trinkets and modified it a bit. The draw_turtles in" my class" just draw "clouds" inthe pictures. It is nothing fancy but just something I am comfortable and be able to work with for now. I plan to explore it further during my Final project which will be involving multiple turtles with similar attributes.
Here is my Class Hack code and trinket
```python
class Draw_Turtle(turtle.Turtle):
  def __init__(self,x,y):
    turtle.Turtle.__init__(self)
    self.hideturtle()
    self.penup()
    self.goto(x,y)
    self.pendown()
    self.color("black")
  def draw_cloud(self):
    self.penup()
    self.right(180)
    self.pendown()
    self.circle(-15,180)
    self.left(90)
    self.circle(-30,180)
    self.left(90)
    self.circle(-15,180)
    self.forward(60)
    self.end_fill()
    self.right(180)
    self.penup()
    
sally = Draw_Turtle(100,100)
johnny = Draw_Turtle(-140,120)
```
<iframe src="https://trinket.io/embed/python/dcb7f3c18a" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>
