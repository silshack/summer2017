---
layout: post
author: samsr31
title: "Sam's Poetry Slam Assignment"
---

Here is my program for the poetry slam assignment:
<iframe src="https://trinket.io/embed/python/84060bf63e" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

Reflection:
After completing the basic requirements for this exercise, I thought through how one might go about checking whether a line was too long, or whether a poem had too many lines.  I came up with two main ways that I could try to solve this; the first would be to measure and standardize the lines, and then stop the user if a line was too long or if the poem went over the total number of lines.  The second would be to detect how long a line was, or how long the poem was, and adapt the screen size accordingly.  Ideally, you would want to let the screen stretch vertically to accommodate infinite lines, and either stretch horizontally, or to use a series of functions to cut overly long lines down into multiple lines.  I tried playing around with resetting the size of the screen in turtle, but wasn’t quite sure if it was doing what I wanted, and so decided to stick with the first option of defining limits for line length.
To do this, I went online to learn a bit about font width, so that I could find what I now know to be called a “monospace” font.  I wanted something where every letter would be spaced the same, so I could reliably calculate whether a line would fit on the page or not.  I was unable to find a list of turtle.write’s accepted fonts, but I tried a few until I found one that definitely was accepted and definitely looked monospaced.
From there, I decided on how much space I wanted to give each line, and then calculated how many lines I could fit inside 400 pixels.  I then wrote a couple lines to check how many lines had been entered, and then A) give the user feedback on how many lines they had left, and B) end the program when they ran out of lines.  I also tried to set these up in such a way that I could come back later and turn the current numbers into variables, so that I could vary this based on chosen font size.
I then did some tests to measure how many letters I could fit horizontally on the screen, and wrote a similar bit of code to check if each line entered was within that size constraint.
Once I had all of this working for one font size, I played around with some other bells and whistles I wanted to try adding.  These included an option to add a title to your poem, different font sizes, and a random text color mode.  The hardest of these to implement was definitely the other font sizes, since I had to test each new font size to find exactly how many characters it could fit on one line, and adjust some variables accordingly.
