---
layout: post
author: businessowl
title: "Aaron Plocharczyk's functional turtles post"
---
<strong>Here's the original copy of the game:</strong>
  <iframe src="https://trinket.io/embed/python/686d92a70f" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>
<br/>
<br/>
<strong>And here's the "functional" copy of the game:</strong>
  <iframe src="https://trinket.io/embed/python/2234acb36d" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>
<br/>
<br/>
<strong>Reflection:</strong>
<br/>
My goal with this assignment was to shorten the length of my code by implementing functions to do some of the repetative stuff for me. I started out by isolating different chuncks of code that I saw being repeated a lot and oraganized them into their own functions that I could just call multiple times, wherever needed. I did this for the functions: getWinner, drawLine, drawMarker, and spin. getWinner returns "X", "O", "Cat", or "". The other functions take parameters. Here are their function signatures:
```
def getWinner()
```
```
def drawLine(x1, y1, x2, y2)
```
```
def drawMarker(x, y, color)
```
```
def spin(color, angle)
```
I then focused on the fact that I was doing essentially the same thing for player X and then for player O in my loop. If I could simply pass "O" or "X" into a function, I could just call that funciton <i>once</i> in the while loop and just toggle O/X at the end of the loop so everything would play out the same way. So I did that. All I have to do in the while loop now is call:
```
drawSymbolAt(currentSymbol, turn)
```
and it will return True or False, based on whether the symbol was successfully drawn or not. As a technical side note, drawSymbolAt just calls a helper function called "drawOrFalse" with appropriate parameters, and "drawOrFalse" does the actual work.
