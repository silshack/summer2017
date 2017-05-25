---
layout: post
author: samsr31
title: "Turtle Hack Post - Sam Robinson"
---

Here is my Turtle Hack program:

<iframe src="https://trinket.io/embed/python/6704f2abf5" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

When trying to think about what the “coolest” program I could write would be, I decided to mess around with the screen.onclick controls demonstrated in the first chapter of our video textbook.  I didn’t have any ideas for a specific drawing to try to create, and so instead I wanted to see if I could recreate the drawing functions from the textbook examples, and add some of my own.  Also, since I am not a particularly dextrous artist, I decided to try restricting tina’s movements in the drawing app, so that I would have more easy to work with angles.  At first, I had tina only turning in full 90 degree angles, but eventually decided to relax this to 45 degrees.  I feel like this gives a pretty good range of motion, while still being easy to judge tina’s position and exact heading.  Also, later on in the process I decided to add some penup and pendown options, as well as fill options.
The biggest roadblock it hit was with color selection.  The video examples showed how to select from a preset list of colors, but I wanted to make this an input prompt, like what we did in our other homework assignments.  However, something about the function I defined causes it to infinitely prompt the user for a color when the color key is hit.  I am not sure what to do to fix this, and plan to bring it up in class.  Sadly, this means that what could be a pretty neat little drawing program is left a little flat, as it can only draw in black.

```
# Bugged section of code
def choose_color():
  x=raw_input("Choose a color")
  tina.color(x)

screen.onkey(choose_color, "c")
```
