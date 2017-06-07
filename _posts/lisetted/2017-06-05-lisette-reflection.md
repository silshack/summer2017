---
layout: post
author: lisetted
title: "Lisette's reflection on class so far"
---

Reflection on class so far:

So far, I've found python programming to be a bit of a roller coaster (mostly in a good way). Some things come easy and are fun. Sometimes I get stuck on something for a long time and it's a slow uphill slog until suddenly I figure out my bug or understand how a function works and then the fun downhill begins!

Several times while I've been working on a project I've found myself stuck in a corner with code that didn't run. In these situations I've tried to take a step back and look at my program with fresh eyes to see how to fix it. Most of these times I've just needed to fix a simple syntax error like a ":" or an indent. Though I have had many individual "ahah" moments while learning new functions or how to apply them, a bigger one is using the technique of stepping back and reading the code both in the big picture of what is going on and reading the details like these syntax issues.

One thing that was fuzzy for me prior to class, and continues to be a little fuzzy is the use of loops. For example, this code below from my clicky turtles exersize. I originally wrote code that required the user to hit enter before moving on to create the shape functions in order (square, circle, triangle, clicky(random shape)), but during class my partner helped me write this loop. However, this loop only seems to ever use the clicky-random-shape fuction and skip all the previous shapes. I'm not sure exactly what to do next with this code to debug it, and since I'm struggling with understanding how the for loop iterates, I've come to a bit of a standstill. While debugging this and my other trinkets, the use of the print function has helped me understand exactly when a function is happening, but I'm still out of idea of with what to try next.

```python
i=0
input("Click in the boxes in order to create shapes. Press enter to begin.")
for i in range(4):
  if i == 0 :
    screen.onclick(square)
      # print("This is a square")
    # i=i+1
  if i== 1:
    screen.onclick(circle)
    # print("This is a circle")
    i=i+1
  if i== 2 :
    screen.onclick(triangle)
    # print("This is a triangle")
    i=i+1
  if i==3:
    screen.onclick(clicky)
  else:
    print("you have come to the end")
 ```
 
For other trinkets, I have felt more successful. For example, the earlier programs we created that were just the turtle drawing at first seemed uncomfortable. I'm used to writing code to manipulate datasets for statistical analysis and doing something "creative" with coding was weird for me. There were many functions that I would never even have thought to look for if I hadn't stumbled while googling solutions for other problems. The code below shows part of a function I created to draw a banjo. I wanted the user to be able to decide not only where to put the banjo, but also how it was positioned on the screen. I struggled with changing the starting angle of the banjo neck, but that created problems because then sometimes the banjo next would cross the round part, or otherwise  look weird. The setheading function fixed that and created an easy way to change the angle of the banjo and something I really never would have thought of on my own. This process has made me cognizant how little I know about python, but also how powerful the language can be when you have more functions in your toolbox. Additiionally, the use of the setheading function helped me understand how the turtle moves based on directions. 

```python
  #body of banjo
  tina.goto(x,y)
  tina.setheading(tilt)
  tina.pendown()
  tina.circle(50, -180)
  tina.circle(50, 180)
  tina.circle(50, 180)
  tina.left(75)
  ```
