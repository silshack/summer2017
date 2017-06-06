---
layout: post
author: Ibbi2010
title: "My reflection on class so far!"
---

Reflection:

I had apprehensions before starting this class.The first day of class put all my worst fears into reality. I tried hard to keep up with the class and went completely numb,thinking what have I gotten myself into. Half way through the course ,I still struggle but at the same time wonder how far have I made it. I feel that I know the concepts but I havn't mastered them yet. The atmosphere of the class is always extremely charged, which is an ideal environment to learn and thrive. The competency of skills shown by our various class mates, is an inspiration but mostly a source of stress with a capital "S". It does not mean that I dont get to learn or admire what others have accomplished. I do try to concentrate on my abilities and take a little comfort in the fact that I have been able to learn something from nothing. The thing which bothers me particularly, is that 'being average' is never my goal.
Honestly, if there ever was a "light bulb moment", I might have completely missed it.There were many small "flickering light moments" though. They usually happen while I am doing chapter exercises and am stuck on something trivial for the longest time and later find out,that the solution was right there in front of me.
Confusing moments are my speciality, since there were so many. While solving "Loops,Lists and Strings" exercises I felt I had to keep going back to the chapters and online videos to make myself understnad the concepts better.It did help me in the end .
I  feel the concepts of "Try and Except" are still a little bit fuzzy to me. I am also trying to get better at the "lists". I do know the theory but I believe I can only get better with continous practice and using the vocabulary as much as I can.
My biggest problem solving strategy is to 'take a break', think over it and come back to the problem with the fresh mind. and when this does not work ,I go ahead and shoot an email to my instructor. Twice it has happened, that, by just doing it led me to the solution.
I would also like to add that one of the major reasons ,I am still surviving the class is an extremely encouraging and accepting attitude of our instructor. sometimes situations get really frustrating and during those times ,the most helpful tools are your patience and communication with the students.

I am adding the codes for my "custom turtle",which is a Newyork Skyline. During this assignment I felt for the first time ever that I can do coding as well:)

```python
import turtle

nael = turtle.Turtle()
nael.speed(6)
myscreen = turtle.Screen()

myscreen.bgcolor("orange")


# base rectangle
nael.color("grey")

# first function
def draw(x,y):
    nael.penup()
    nael.goto(x,y)
    nael.pendown()
    
# second function
def move(length1,angle1,length2,angle2):
    nael.forward(length1)
    nael.right(angle1)
    nael.forward(length2)
    nael.left(angle2)
    

draw(-200,-110)
nael.begin_fill()
nael.forward(410)
nael.right(90)
nael.forward(100)
nael.right(90)
nael.forward(410)
nael.right(90)
nael.forward(100)
nael.end_fill()
nael.penup

#first building(left)
nael.color("black")
nael.begin_fill()
move(40,90,10,90)
nael.forward(20)
nael.right(90)
move(30,90,10,90)
move(10,90,10,90)
nael.forward(10)

# second building
nael.left(90)
nael.forward(20)
nael.right(90)
move(20,90,20,90)
nael.forward(10)
nael.left(90)

# third building
nael.forward(30)
nael.right(90)
nael.forward(4)
nael.circle(3)
move(4,90,4,90)



# 4th building
move(5,90,2,90)
nael.forward(5)
nael.left(90)
move(7,90,10,90)
move(10,90,6,90)
move(20,90,3,90)
move(10,90,3,90)
nael.forward(5)
nael.right(90)
move(10,90,5,90)
move(3,90,10,90)
move(3,90,20,90)
move(6,90,20,90)
move(3,90,5,90)
move(4,90,8,90)

#between 4th building and Empire state building

nael.forward(7)
nael.left(90)
move(9,90,10,90)


#Empire State Building

move(10,90,10,90)
move(100,90,5,90)
move(20,90,5,90)
move(15,90,2,90)
move(10,90,10,90)


# top of ESB

move(10,90,20,95)
move(90,190,89,95)
move(20,90,10,90)
move(10,90,10,90)
move(2,90,15,90)
move(5,90,20,90)
move(5,90,142,90)

#between Empire and Chrysler
nael.forward(4)
nael.left(90)
nael.forward(90)
nael.right(90)
move(50,90,4,90)
nael.forward(6)
nael.right(90)
nael.goto(125,-20)

#Chrysler
nael.left(90)
nael.forward(20)
nael.left(90)
move(12,90,4,90)
nael.forward(12)
nael.right(90)
nael.forward(4)
nael.goto(160,30)
nael.left(88)
nael.forward(20)
nael.left(183)
nael.forward(20)
nael.goto(160,30)
nael.left(0)
nael.forward(25)
nael.left(90)
move(4,90,12,90)
move(4,90,15,90)
move(4,90,60,90)
nael.forward(4)
nael.left(90)
nael.forward(40)
nael.right(90)
move(10,90,10,90)
nael.forward(15)
nael.right(90)
nael.forward(60)
nael.end_fill()

#I love Ny

draw(-180,140)
nael.color("red")
def write():
    return("I love Newyork")
write()
nael.write("I LOVE NEWYORK",None,"16pt bold")
```

This other code is for one of the conditional exercises,
```python
# This line gives prompt to enter score

score=float(input("what is your score"))
score > 0.0 and score < 1.0

# Error statements

if score < 0.0:
    print("scores are between0.0 and 1.0 ")
if score > 1.0:
    print("Please check the range of score")

# scoring

if score >= 0.9:
    print("A")
elif score >= 0.8:
    print("B")
elif score >= 0.7:
    print("c")
elif score >= 0.6:
    print("D")
elif score < 0.6:
    print("F")
else:
    print("scores are between0.0 and 1.0")
  ```
  
