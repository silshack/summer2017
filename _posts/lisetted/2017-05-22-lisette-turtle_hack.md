---
layout: post
author: lisetted
title: "Lisette's Turtle Exercise"
---

Here's the program I'm embedding:
<iframe src="https://trinket.io/embed/python/8eb5179d7f" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>


Reflection:

I didn't recieve Elliot's email about creating a turtle hack before class, so I just copied a turtle (Turtle in space, https://trinket.io/library/trinkets/3bdab3639b) that was on the front page of trinket. After skimming the comments (not really the code:() to understand what the turtle was doing, I decided that I wanted to have the space ship draw as it moved. On my first attempt I tried adding the code for the line towards the beginning after the def statements.

```
# these defs control the movement of our "turtle"
def forward():
  turtle.forward(move_speed)

#draw lines behind spaceship
turtle.pendown()
turtle.color("yellow")
```

However, this was not the correct place to put it! This turned the screen white, with a yellow trangle for the spaceship and no lines being drawn. I checked the code again closely and noticed I didn't see all the code towards the bottom because I didn't scroll all the way down on both my browser and the code (rookie mistake!). At line 36, the original turtle author had the pen go up and return home, and then gave commands that move the turtle. I realized that after these pieces of code was the correct location to put the pendown to have the spaceship turtle draw where it is going and to do it in yellow. During class I showed my turtle hack to my partner, who suggested that I also make the line thicker to make it easier to see.
I made fairly simple change to this turtle, but I did learn that I should read code and comments more carefully and really understand all the steps the code is making before I try to make any changes to it.
 
