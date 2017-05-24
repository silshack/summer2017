---
layout: post
author: kmorbitzer
title: "Kathryn's functional turtle post"
---

Here's my original program:
<iframe src="https://trinket.io/embed/python/092f2a4410" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

Here's my new program:
<iframe src="https://trinket.io/embed/python/e81d9059d2" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

Here's my reflection:
For the functional turtles exercise, I chose to create functions in my logical turtles program.  This was something that was challenging for me.  I first had to decide which functions to put in. The function that creates an argument was easier to do, as I created a function that would create the circles.  The next function was more challenging to come up with and I ended up deciding to try to make the circles different colors randomly.  To do this, I needed to import the random module.  This then allowed me to create a return function that would fill in the circles as different colors in a random order.  
The code ended up not doing exactly what I wanted, as I wanted the circle to fill in a color, and then the next circle filling a color behind the original circle.  However, I remembered that once a new shape is created and filled in, it will cover an overlapping shape.  Therefore, the program ends up creating a circle, filling in a color, then creating a bigger circle, and filling in that circle’s color over the original circle, etc.  Not quite what I was aiming for, but still allowed me to practice incorporating functions. 
