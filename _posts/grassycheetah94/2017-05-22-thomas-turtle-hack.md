---
layout: post
author: grassycheetah94
title: "Thomas' Turtlehack"
---

Here is the program I am embedding:
<iframe src="https://trinket.io/embed/python/2a682241b6" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

---
Reflection:
I wanted to create a turtle version of the ‘Hello Chuck’ assignment we had this weekend. I started with creating a ‘man’. This took a lot longer than I originally thought it would, so he is not as detailed as I wanted him to be.  But the basic concept is still there. As you can see below.

```
#Mouth
jack.goto(25,15)
jack.pendown()
jack.goto(20,10)
jack.goto(-20,10)
jack.goto(-25,15)
jack.penup()
#Nose
jack.goto(7,35)
jack.pendown()
jack.goto(5,33)
jack.goto(3,35)
jack.goto(0,30)
jack.goto(-3,35)
jack.goto(-5,33)
jack.goto(-7,35)
jack.penup()
#Eyes
jack.goto(17,50)
jack.pendown()
jack.fill(True)
jack.circle(4)
jack.fill(False)
jack.penup()
jack.goto(-17,50)
jack.pendown()
jack.fill(True)
jack.circle(4)
jack.fill(False)
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
#Ears
ell.goto(42,45)
ell.pendown()
ell.fill(True)
ell.goto(42,60)
ell.goto(43,62)
ell.goto(45,63)
ell.goto(47,62)
ell.goto(48,60)
ell.goto(48,45)
ell.goto(47,43)
ell.goto(45,42)
ell.goto(43,43)
ell.goto(42,45)
ell.fill(False)
ell.penup()
ell.goto(-42,45)
ell.pendown()
ell.fill(True)
ell.goto(-42,60)
ell.goto(-43,62)
ell.goto(-45,63)
ell.goto(-47,62)
ell.goto(-48,60)
ell.goto(-48,45)
ell.goto(-47,43)
ell.goto(-45,42)
ell.goto(-43,43)
ell.goto(-42,45)
ell.fill(False)
ell.penup()
#Hat
jack.speed(0)
jack.goto(37,60)
jack.fill(True)
jack.goto(80,60)
jack.goto(80,65)
jack.goto(37,65)
jack.goto(32,95)
jack.goto(-32,95)
jack.goto(-37,65)
jack.goto(-80,65)
jack.goto(-80,60)
jack.goto(37,60)
jack.fill(False)
jack.penup()
jack.goto (0,-150)
jack.penup()
```

The user is asked their name and the ‘man’ responds to this answer by greeting him, then asking the weather. Then responding to that response, he answers in the affirmative. Then the ‘speaking man’ says he has to go and BYE! As seen below.

```
#Whats your name?
ques_name = raw_input("What is your name?")
jack.color("white")
jack.goto(25,-50)
jack.fill(True)
jack.goto(13,-5)
jack.goto(40,-40)
jack.goto(25,-50)
jack.fill(False)
jack.penup()
jack.goto(40,-175)
jack.fill(True)
jack.circle(75)
jack.fill(False)
ell.goto(40,-90)
ell.write("Hello", None, "center", "25pt bold")
ell.goto(40,-125)
ell.write(ques_name, None, "center", "25pt bold")
```

That looks like:
![Turtle image](http://i.imgur.com/9xhxzKr.png)

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
ell.write(ques_weather, None, "center", "15pt bold")
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

That looks like:
![Turtle image](http://i.imgur.com/raFvMnq.png)
![Turtle image](http://i.imgur.com/xs8iIOu.png)
![Turtle image](http://i.imgur.com/lSntLnU.png)

The only problem I ran into was figuring out how to have user input be placed into a sentence along with non-user inputted words. So I was forced to figure out correct spacing between user imputted words and auto imputted words. Which, actually I like better.

-grassycheetah94

