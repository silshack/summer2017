--- 
layout: post
author: nurahill
title: "Nura's Poetry Slam"
---

Here is my code:

<iframe src="https://trinket.io/embed/python/70fa7f1f09" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

This, as usual, took me sometimes to put together. I spent a lot of time trying different things that were not working. This part (shown below) took the longest time:
```
for i in words:
  tina.write(i, align="center", font=("Arial",  30, "normal"))
  y = y - 40
  tina.goto(0, y)
```
I kept putting whats below, inside of the for loop above:
```
y = 160
tina.goto(0, y)
```
I finally realized after moving things around that the y variable outside of the for loop, made it work properly.

I also spent some time trying to figure out how to change the font, size and color of my text. I figured out how to change the font and size, then soon realized that the color changes when you change the color or the turtle... lightbulb moment! or more like, duuuuhhh moment. :)

