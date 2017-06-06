---
layout: post
author: jpanken
title: "Jaffa's Reflection on Learning Python"
---

Sometimes learning python has been exhilarating; sometimes it has been exhausting.  When I tried to make a filled star by hand, it was exhausting.  I changed the measurements for every angle and every line:
```python
#draw triangle 3
ninja.fill(True)
ninja.right(118)
ninja.forward(70)
ninja.left(146)
ninja.forward(75)
ninja.left(110)
ninja.forward(40)
ninja.fill(False)
```
I probably could have googled more and found a more elegant solution, but I wanted to do it the hard way.  Doing it the hard way is exhausting, but I definitely learn more as a result.


When I did my original Turtle Treasure Hunt, I couldn’t make the clicking work correctly.  So I spent a couple more days on it and got it to work.  I was still having trouble with repetitive stamping, which I figured was an animation effect.  Eventually, I figured out that I need to turn the “tracer” off before the turtle moved.  Then, I couldn’t get the “congratulate” function to work.  Again, it took me a while to pinpoint the tracer as the issue and turn it back on after the play won the game:
```python
while user_has_won:
  hunter.goto(0, 0)
  hunter.pendown()
  myscreen.tracer(1)
  congratulate(myscreen, hunter, treasure, scribe)
  user_has_won = False
```
I had to understand how the tracer worked before I could put all the pieces together and make it work.  I learned not to put in code just willy-nilly, I needed to understand what it does and how it works.


I’m still having trouble understanding how to make functions defined in the helper code work in the main window.  I’ve tried to be careful about using filler parameters and defining the actual parameters in the main window, but I can’t seem to make the more complex code actually work.


Most of the time, my “go to” problem solving strategy is to print as I go along.  This helps me ensure that the program is working appropriately step-by-step.  Another problem solving strategy includes opening a copy and working on the issue in a completely different way without consequences for my original program.  I also need to remember to take breaks more often.
