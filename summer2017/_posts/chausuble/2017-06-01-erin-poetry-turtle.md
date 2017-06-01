--- 
layout: post
author: chausuble
title: "Erin's Treasure and Mine Turtle"
---

<iframe src="https://trinket.io/embed/python/7690615bcc" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

My first goal was simply to add strings to the list - .append didn't work, but + [] did, go figure - then have the 
program write the strings starting from the top left. When that was done, I made them into a while loop, which would 
append strings to the list until the user wrote "done." So the basic part of the assignment worked out. I used that to figure
out how many lines the screen could have at once, and counted how many letters could show up on one line. Handling the lines
was fine, but I had to compromise splitting the lines - rather than cutting up the lines neatly, I just truncated them. Trying
to slice the lines resulted in disaster since I overshot my bounds and tried to get all fancy using the "%" sign to determine
the number of lines to write...well! I'll probably try to work it out in my spare time, and do an ETA with the new turtle if
I can get it done before midnight. Probably not!

So the main assignment itself wasn't too stressful - just trying to do all of the extra tchotkes. 

Ideas for improvements: 

Find the last " " in a line and break off line there, printing the rest of the contents on the next line, to not break up lines in the middle of words

Have the program print the poem if the user wants, so they can save it. Maybe even have multiple pages?!

Rather than truncating lines, have the program tell how many characters are in a line, divide them by 35 to see how many lines they would be, and then add those lines to the poem list

Don't know how I would do it, but have the program tell the user how many characters are being used in the currently-written line
