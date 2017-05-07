---
layout: post
author: elliott
categories:
  - exercise
title: Clicky Turtles Exercise
---

Submit a well-formatted pull request to our class blog with embedded Trinket programs for the below exercises.
Complete these on your own, using any materials you need. Do not
look at other students' submissions until after you've completed your work.  

**After your programs are done**, check other students' work and other resources online if you had questions.
Include a reflection about what you think you've learned and any concepts that are still fuzzy to you.
Did you encounter frustrating situations? Did you feel a lightbulb turn on?

___

This is another open-ended turtlehack, but now you've got lots of tools in your
toolkit.  Take the weekend and, instead of watching that dumb Super Bowl, code
an awesome program.  Don't forget your Problem Solving Attitudes and Strategies!

Write a turtle program that:  

* Has a `setup()` function that sets up your screen visually. For instance, you could
draw green grass and blue sky using the `.fill()` method. I've created a second
* Uses the `screen.onclick()` function method to call `clicky()` function you create
* Within clicky, do something cool.  Think outside the `.goto(x, y)` box :)
* Within clicky, **call** one or more helper functions you've created
* Within clicky or helper functions, use logic to change your program's behavior
based on the turtle's x and/or y coordinates.  For instance, you could vary the 
turtle's color, speed, or call different helper functions.
* Does one of the following:
  * Allows the user to make something creative interactively
  * Has a 'win' condition.  Make sure to give instructions!
  * Implements a narrative animation.  `import time`, `time.sleep(x)` and `tina.clear()`
will be useful if you pick this one.

If you'd like to stretch yourself, try these:  

* Add other functions to `animations.py`, import them and use them in your main
program.
* Create a second turtle other than `tina` and have him/her also do something
in your clicky function.
* Explore the `screen.update()` and `screen.tracer()` methods to change how
often the screen updates and fix the zigzag artifacts.
* Add your own new module (i.e. `mymodule.py`) and `import` something from it.
You could even put your clicky function there to keep your code clean and readable.


Use this starter code unless you feel like coding from scratch:

<iframe src="https://trinket.io/embed/python/fbf0c594fd" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>