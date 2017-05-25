---
layout: post
author: WildGinger23
title: "WildGinger's Turtle Exercise"
---

Here's the program I am embedding

<iframe src="https://trinket.io/embed/python/25ffca8e3f" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>


This is an example of how I coded orders to display at the top of the page, then dissapear.

```
#Orders(2)
strato.goto(0,150)
strato.write("Bomb Turtlopolis!", None, "center", "16pt bold")
strato.goto(0,0)
strato.color("dark blue")
strato.goto(0,150)
strato.write("Bomb Turtlopolis!", None, "center", "16pt bold")
strato.goto(-150,-150)
```


Reflection


Hello all, meet the Boeing B-52 Stratofortress, nicknamed strato.
I wanted to go beyond colors and explore some of the other things that turtles can do, so I set out to stick with a two-tone color scheme (with the exception of the evil Turtlopolis).
The "dark blue" and "light green" reminded me of a radar screen display, so I decided to make a flightplan.
I begin with an arrow to represent the B-52 bomber, however, I hid the icon to make text display at the top and couldn't get it to come back.
So the plane entered stealth mode and its location was charted with penup() and pendown()
I decided to make the target of the bomber Turtlopolis, an evil city shaped like a turtle.
The B-52 bomber executed three looping bombing manuevers, which brought it beyond the scope of radar, in three parallel paths above the city.
Tutrtlopolis was destroyed.
