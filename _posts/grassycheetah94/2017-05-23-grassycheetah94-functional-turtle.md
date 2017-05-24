---
layout: post
author: grassycheetah94
title: "Thomas' Functional Turtle"
---

The original turtle:
<iframe src="https://trinket.io/embed/python/2a682241b6" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

The new and improved turtle:
<iframe src="https://trinket.io/embed/python/ed38169ed6" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

What I changed: 
```
#Jaw
ell.pensize(2)
ell.goto(38,45)
ell.pendown()
ell.goto(38,10)
ell.goto(20,-5)
ell.penup()
ell.goto(-37,45)
ell.pendown()
ell.goto(-38,10)
ell.goto(-20,-5)
ell.penup()
ell.goto(-7,-10)
ell.pendown()
ell.goto(-5,-13)
ell.goto(5,-13)
ell.goto(7,-10)
ell.penup()
```
to
```
#Jaw
def jaw(x,y):
  ell.pensize(2)
  ell.goto(x,45)
  ell.pendown()
  ell.goto(x,10)
  ell.goto(y,-5)
  ell.penup()
jaw(38,20)
jaw(-38,-20)
#Chin
def chin():
  ell.goto(-7,-10)
  ell.pendown()
  ell.goto(-5,-13)
  ell.goto(5,-13)
  ell.goto(7,-10)
  ell.penup()
chin()
```
and...
```
#Sideburns
jack.penup()
jack.goto(37,45)
jack.pendown()
jack.fill(True)
jack.goto(41,45)
jack.goto(41,60)
jack.goto(37,60)
jack.goto(37,45)
jack.fill(False)
jack.penup()
jack.goto(-37,45)
jack.pendown()
jack.fill(True)
jack.goto(-41,45)
jack.goto(-41,60)
jack.goto(-37,60)
jack.goto(-37,45)
jack.fill(False)
jack.penup()
```
to
```
#Sideburns
def sideburns(x,y):
  jack.penup()
  jack.goto(x,45)
  jack.pendown()
  jack.fill(True)
  jack.goto(y,45)
  jack.goto(y,60)
  jack.goto(x,60)
  jack.goto(x,45)
  jack.fill(False)
  jack.penup()
sideburns(37,41)
sideburns(-37,-41)
```
and finally....
```
#Weather?
ell.penup()
ell.speed(2)
ell.goto(40,-175)
ell.color("white")
ell.fill(True)
ell.circle(75)
ell.fill(False)
ell.color("pink")
ell.goto(40,-90)
ell.write("How is", None, "center", "20pt bold")
ell.goto(40,-125)
ell.write("the weather?", None, "center", "20pt bold")
ques_weather = raw_input("How is the weather?")
ell.goto(40,-175)
ell.color("white")
ell.fill(True)
ell.circle(75)
ell.fill(False)
ell.goto(40,-80)
ell.color("pink")
ell.write("I agree", None, "center", "15pt bold")
ell.goto(40,-105)
ell.write("the weather is", None, "center", "15pt bold")
ell.goto(40,-130)
ell.write(ques_weather + "!", None, "center", "15pt bold")
ell.goto(40,-175)
ell.color("white")
ell.fill(True)
ell.circle(75)
ell.fill(False)
ell.goto(40,-80)
ell.color("pink")
ell.write("Sorry, but", None, "center", "15pt bold")
ell.goto(40,-105)
ell.write("I have to go.", None, "center", "15pt bold")
ell.goto(40,-130)
ell.write("BYE!", None, "center", "15pt bold")
```
to
```
#Weather?
ell.penup()
ell.speed(2)
def bubble():
  ell.goto(40,-175)
  ell.color("white")
  ell.fill(True)
  ell.circle(75)
  ell.fill(False)
  ell.color("pink")
  ell.goto(40,-80)
bubble()
ell.goto(40,-90)
ell.write("How is", None, "center", "20pt bold")
ell.goto(40,-125)
ell.write("the weather?", None, "center", "20pt bold")
ques_weather = raw_input("How is the weather?")
bubble()
ell.write("I agree", None, "center", "15pt bold")
ell.goto(40,-105)
ell.write("the weather is", None, "center", "15pt bold")
ell.goto(40,-130)
ell.write(ques_weather + "!", None, "center", "15pt bold")
bubble()
ell.write("Sorry, but", None, "center", "15pt bold")
ell.goto(40,-105)
ell.write("I have to go.", None, "center", "15pt bold")
ell.goto(40,-130)
ell.write("BYE!", None, "center", "15pt bold")
```
Reflection:
To sum it up I defined a function for drawing the jaw (jaw(x,y)), chin (chin()), and sideburns(sideburns(x,y)); as well as a function that redraws the speach bubble, labeled bubble(). Both the jaw and sideburn functions have arguements to change from positive x values to negative x values and thus have symmetry. Overall the toughest thing was figuring out how to define each arguement and decide what could be defined as an arguement. Also not everything that could be defined made the code any shorter so I took away a lot of definitions I originally created (except chin()).
