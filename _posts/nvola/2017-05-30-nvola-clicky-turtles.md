---
layout: post
author: nvola
title: "Natasha's Clicky Turtle Exercise"
---

Here is my Clicky Turtle Exercise:


<iframe src="https://trinket.io/embed/python/3fce5e4d21?start=result" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>


The game is very simple: the player is a turtle, there are 3 "noms" to feed the turtle, and the user has to use the arrow keys to navigate the turtle to the noms to feed the turtle. The goal is to get all 3 noms in 10 moves or less (only moves forward or backward are counted as moves, turning the turtle doesn't count as a move). When the user presses 'enter' to start the game, the three noms and the turtle are placed at random coordinates on the playing field. Additionally, the turtle can move faster when it's "swimming through the water" versus when it's "waddling through the sand"; this was easy to implement once I looked at the Python documentation and saw the ```.ycor()``` function. I got the idea for this game as kind of a mix between the classic snake game and the treasure hunt turtle exercise we did last week. So I started by coding the turtle and the food, then I decided I wanted to do a beach background, and that's where I got the idea to have the turtle move different speeds depending on it's location on the playing field. Then I got into coding the key presses and the move counts and nom counts that determine whether the player wins or loses.


A small difficulty I came across was in dealing with the local versus global variable. There were a few variables that needed to be used outside the function (the count of how many moves the user had made, the number of noms eaten), however to make the game play code easier to read I wanted the functions to do all the leg work, but once I worked that out for one of the variables it was easy enough to use for the other. Relatedly, I had to set a start number for distance and arbitrarily chose 10. But for some reason, the code doesn't always count the distance between the nom and the turtle as being close enough, even though it's supposed to check the distance between the turtle and each nom every time it moves, if the distance is less than 5 turtle moves or less it's supposed to count as having eaten the nom but it doesn't always count it. Not sure why. Code is below:

```
distance2 = 10
distance3 = 10
distance4 = 10
def check_distance():
  global distance2
  global distance3
  global distance4
  distance2 = t1.distance(t2)
  distance3 = t1.distance(t3)
  distance4 = t1.distance(t4)
  if distance2 <= 5:
    t2.hideturtle()
    count_noms()
    print('You ate one noms. Nom count: {0}'.format(nom_count))
  if distance3 <= 5:
    t3.hideturtle()
    count_noms()
    print('You ate one noms. Nom count: {0}'.format(nom_count))
  if distance4 <= 5:
    t4.hideturtle()
    count_noms()
    print('You ate one noms. Nom count: {0}'.format(nom_count))
```

Also, I tried to have a different screen at the end of the game, but couldn't get that to work; I'm not sure I have the ```.setup()``` function working correctly, so that might be what's causing the issue. Since I couldn't get that to work, I chose to deactivate the key presses when the game is over so  that the user can't make any more moves. I also wanted to make it so that the turtle couldn't go off the playing field, but couldn't find a good way to quickly incorporate that into my existing code that was checking for the y coordinates to determine how far forward or backward the turtle could move. 
