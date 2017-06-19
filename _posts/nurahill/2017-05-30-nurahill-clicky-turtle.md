--- 
layout: post
author: nurahill
title: "Nura's Clicky turtle excercise"
---

Here is my code for option 1:
<iframe src="https://trinket.io/embed/python/3c8744a1ac" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

On option one, as usual, it took me a bit to come up with an idea of a program for this one. I ended up deciding to draw a ground and sky. on lines 38-46 i created my clicky funtion. I made it so if tinas y coordinate of the place you click on is greater than -152 it would draw a star (on the sky), and if it was less than it would draw a flower (on the ground). My helper functions are the star and flower. 

Here is my code for option 2:
<iframe src="https://trinket.io/embed/python/b8a6b80918" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

I wasnt able to get to do a whole lot with option two. I bascially was just able to make it work, as it took me sometime to get it working properly. I created the list of colors so by clicking on shift, the turle color would change to different colors. Below is where i was able to use randint to make it choose a random color. where it says [randint(0,len(color)-1)] it means that I want it to pick a random color (randint) from 0 to the length of color, -1 (-1 makes sure that it never picks a color out of range)
```
# Define a function to change the color
def color_change():
  tina.color(colors[randint(0,len(colors)-1)])
```
I feel like this excersice was a good foundation to build on futher in the future. Its pretty cool to able to manipulate the turtle with the keyboard and make it draw things. I particularly like that penup and pendown part that i created (wich you can turn on or off by clicking 'u') becaue that gave me the ability to draw things (like a square, triabgle, etc.). Th e penup/pendown was my something creative!
