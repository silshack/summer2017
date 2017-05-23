---
layout: post
author: neatoskeeto
title: Matt's Turtle Dart Game
---


<iframe src="https://trinket.io/embed/python/e2775efcac" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

The hardest part about this program was getting the logic of the color selection in the beginning. Before I used a try/except sequence, I tried a bunch of different ways to get it to check to make sure the input was a number first. 
I tried nonsense statements like:
```
if type(float(judit_color)) != int or float:
  judit.color("red")
```

I finally tried to do the try/except method, which worked out nicely.
I would like to make a loop to restart it if the user inputs an invalid number or name, and maybe use a random number generator to make the game more fair. My wife's name is Judit, so she can't win the game because she has an odd number of letters in her name.
