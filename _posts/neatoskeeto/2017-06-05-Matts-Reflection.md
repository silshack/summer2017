---
layout: post
author: neatoskeeto
title: "Matt's Reflection on the class so far"
---

I am much less confident today than I was when we started this class a couple weeks ago. I feel like in order to do the exercises for the next class, we have to learn more about python or loops than what we read in that night's reading. For instance, for the Romeo assignment, one of the students knew that a way to get all of the words into a list was to use the read() method, but we didn't learn about read() until last night's chapter!

I find myself more easily giving up when I can't figure out what is wrong with my program. I think it might have something to do with being tired, especially towards the end of the week.

One lightbulb that went off for me was when in class you went over functions that returned 2 things and printed two things and we saw what happened when you commented out one of the print statements. I realized that the print was different from the return values.

Another aha moment came from my TurtleHack, where I realized I could make lines of growing width appear like tear drops.
```
#tear
tina.goto(23,127)
tina.color("blue")
tina.pensize(1)
tina.pendown()
tina.right(39)
tina.forward(3)
tina.pensize(3)
tina.forward(3)
tina.pensize(6)
tina.forward(2)
tina.pensize(8)
tina.forward(4)
tina.penup()
```
I had to guess and check the direction the turtle was facing to make sure it was going straight down. I didn't know about setheading, which would have made it a lot easier.

Another aha moment I had was from the class exercise where we had to calculate the median value from a list of numbers. I knew that for lists with even numbers of items, the median would be the average of the middle 2 values, but I kept getting the wrong answer when I tried it. I realized that because the list starts at index value 0, I needed to subtract 1 from my list[i] to find the "lower middle" item in the list needed to calculate the median.

```
if i%2 != 0: #if there's an odd number of numbers in the list
  median = int(i/2) #takes advantage of rounding up odd numbers
  median_value = x[median]
else: 
  median = int(i/2)
  even_median_upper = float(int(x[median-1])) #tricky! because the index starts at 0, I have to subtract 1
  even_median_lower = float(int(x[-median]))
  y.append(even_median_lower)
  y.append(even_median_upper)
  #print(y)
  median_value = sum(y)/2
  ```
  I try to print things in between steps to help me make sure the program is doing what I want it to. I also like to ask classmates, and they often have great advice.
  
  I hope the second half of this course things start to gel more for me.
