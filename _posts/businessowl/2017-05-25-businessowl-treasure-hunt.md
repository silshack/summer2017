---
layout: post
author: businessowl
title: "Aaron Plocharczyk's treasure hunt post"
---
<strong>Here's the game:</strong>
  <iframe src="https://trinket.io/embed/python/c16fb5cea8" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe><br/>
<br/>
<strong>Reflection:</strong>
<br/>
I started out by meeting the bare minimum requirements (taking keyboard input, printing how close you were, and printing "you win") and then decided to do more with it. I accepted click input instead of keyboard input (which kind of forced me to discard the while loop and make all that stuff into a function that gets called every time the user clicks) and then added stuff to the game that I thought would be nice. The first thing I thought would be cool was to make the turtle point to your cursor before it goes to it. That turned our to be VERY challenging and included a lot of geometry and a global varible. The global variable keeps track of the turtle's current rotation state so once I figure out what the degree should actually be, I can offset that number by the turtle's current rotation and end up with it pointing the right direction.<br/>
Next, I thought it would be useful to drop a marker everytime Tina got the closest to the treasure that she has ever been. That way the player can better trace their way towards the treasure. I had to include a note about what all those markers were signifying, so I wrote it in the beginning of the code, where I outline the game's boundaries (since the game only uses a portion of the screen, and I wanted those boundaries to be clearly defined).<br/>
Other features that I then decided to include are, in order, as follows: Make tina more transparent as you get farther away from the treasure. I did this by defining Tina's color in an "rgba" format, where the "a" part represents opacity. For a semi-transparent black, for example, that looks like this:
```
tina.color("rgba(0,0,0,.5)")
```
I also make Tina draw a yellow circle representing the treasure when the player finds it. And I make the outside of the game boundaries flash a subtle red and have Tina shake her head when the user clicks outside the game's boundaries. That is my favorite part actually. Try it out if you want.
