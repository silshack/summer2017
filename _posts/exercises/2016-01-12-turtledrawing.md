---
author: elliott
layout: post
title: Turtle Drawing!
categories: exercise
date: 2016-01-14
---

These two exercises are all about diving into python and getting our hands dirty.  The first is getting a 
program to ask for user input.  The second is to make the coolest Turtle program you can and post it to 
our blog.  

## Custom Input for Turtles

Make a program that:

* prompts the user for a color and makes a Turtle that color
* prompts the user for a background color and makes it that color

To prompt the user for input we'll need Python's `raw_input()` function.  We haven't learned about 
functions yet, but since we're diving in we're just going to use it and see what happens.

Read up a little on some of the results from a quick Google search:

* Python's [official docs](http://docs.python.org/2/library/functions.html#raw_input) for `raw_input`
* [Stack overflow question](http://stackoverflow.com/questions/5563089/raw-input-function-in-python)

Like much of the documentation we'll find in programming, these imply or depend on a lot of background 
knowledge you may or may not have.  Push on even if you don't understand and see what happens in the 
code!  I'll mention a few things that might help.

`raw_input` gets a value, and we have to store it somewhere to use it in our program.  That's why in 
the example on Stack Overflow there's an assignment of the statement to a variable.  For example, we 
might store the result like this:

```
tina_color = raw_input("What color should Tina be?")
```

This will cause a window to pop up asking "What color should Tina be?" and save the user input into 
the variable.  We can then use the `tina_color` variable later, in place of something like `"red"` or etc.

Using this information, knock out the two components of the exercise above.

## Turtlehacking

Now that we know a little about how to make Turtles do cool stuff, let's [hack](http://paulgraham.com/gba.html) them!

The Turtle library is code that someone else wrote for us.  You can see the full extent of that code 
[here](http://silshack.github.io/fall2013/turtle.html). We went over lots of the Turtle module's functionality 
[in class]({{ site.baseurl }}/exercise/how-to/turtle-basics.html), and you can find more if you're interested online.

Use what we learned and what you discover about turtle to make a **second** program.  This program should be
as cool as possible, whatever that means to you.  During the next class we'll embed this program into 
a post on our class blog and there will be an opportunity for quick code talks to show off what you did.