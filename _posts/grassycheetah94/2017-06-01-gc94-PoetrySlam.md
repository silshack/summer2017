---
layout: post
author: grassycheetah94
title: "Thomas Newlin's Poetry Slam"
---

The code:
<iframe src="https://trinket.io/embed/python/d53d9466f8" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

Reflection:

I started by defining the turtles and making a poetry slam banner at the top using the 'slam' turtle just because I thought it should look like a real poetry slam show. I then instructed the user to select the background color and font color. Then I used the same strategy I used in the 'total, count, average' exercise to collect a series of text inputs by the user, until they type “done”. I then instructed tina to write whatever the user said on the screen. In the loop, after tina writes what the user inputs she then moves forward 30 (I rotated her 90 degrees right at the beginning). She starts from (0,125). I figured out that using 20pt bold font tina could write full words until she got to (0,-175). So I defined a fuction called check(y). The code is stated below (lines 42-27 of my code). I figured out that I had to define the function in the loop or else it did not work. I then added an if statement that if check(y) == false the loop would break. This was definitely my lightbulb moment. It didnt take terribly long because most of my code was just refurbished from other exercises but it took about 45 minutes of guess and check to create the boundaries. 

```
y = tina.ycor()
 def check(y):
    if (y>-176):
      return True
    else:
      return False
  check(y)
```
	
