---
layout: post
author: elliott
categories:
  - exercise
title: Treasure Hunt Turtles Exercise
---

Submit a well-formatted pull request to our class blog with embedded Trinket programs for the below exercises.
Complete these on your own, using any materials you need. Do not
look at other students' submissions until after you've completed your work.  

**After your programs are done**, check other students' work and other resources online if you had questions.
Include a reflection about what you think you've learned and any concepts that are still fuzzy to you.
Did you encounter frustrating situations? Did you feel a lightbulb turn on?

___

Create a program that 

* Creates a hidden treasure at a random location
* Asks the user for X and Y coordinates (and handles bad input) 
* Sends a turtle to those coordinates
* Gives the user feedback on how close they are to the treasure (e.g. changes the turtle's Color, changes the Screen's background color,
writes a message to the screen)
* If the user is within 5 pixels of the treasure, they win.  Play the congratulations animation

I've made some starter code for you to **Remix** that includes the animation and random elements you'll need:

<iframe src="https://trinket.io/embed/python/cfa7c2db9b" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

This sample code uses some things we haven't seen yet:

The `while` loop is something we haven't covered yet, but it repeats as long as the
expression after it evaluates to `True`.  We exit the loop when the user has won.

The `random` module is one we haven't seen yet, but is very useful in Turtle programs.
I use it to generate random numbers for you and in the animation.

The `animations.py` file is a **custom module**.  Custom modules are basically a way of organizing
code so it's more managable. I `import` the function instead of defining it in `main.py`,
getting it out of the way.

# Get Creative!

As our first **game sketch**, this assignment offers lots of opportunity to get creative.
Make sure to pace yourself and run your code often if you're experiementing. You can 
**Duplicate/Make a Copy** of your code on Trinket if you want to experiment without
worrying about breaking your assignment.