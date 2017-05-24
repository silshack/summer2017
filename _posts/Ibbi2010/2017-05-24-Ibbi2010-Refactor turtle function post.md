---
layout: post
author: Ibbi2010
title: "Refactor Turtle Function post"
---
Reflection:
The program I made for custom turtle exercise had many repetitive codes.I thought this would e the best way to concise it down and make the codes more readable. I discovered the codes I have used most are,
```
nael.forward()
nael.right()
nael.forward()
nael.left()
```
I used these four code lines and defined a function "move()". The challenging part for me was to figure out the way to execute the function with various lengths and angles since they were many. After trying myself for quite a bit,I looked it up online and found the answer to my dilemma. 
```
def move(length1,angle1,length2,angle2):
    nael.forward(length1)
    nael.right(angle 1)
    nael.forward(length 2)
    nael.left(angle 2)
```
From there one,I thought everything will be a breeze but I stumbled many times ,it was a lengthy and tedious process. I messed up with all the codes and had to restart again and again.I am still a little unsure about the "return" aspect of the function and wasnt sure how to incorporate that into my exercise.I still was able to reduce my 250 codes program to around 150 codes.
original turtle:
<iframe src="https://trinket.io/embed/python/ce9dd159b5" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>
Refactored Functional turtle:
<iframe src="https://trinket.io/embed/python/47b3a0e357" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>
