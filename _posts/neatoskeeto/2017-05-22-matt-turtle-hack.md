--- 
layout: post
author: neatoskeeto
title: "Matt's TurtleHack Inspired by Oz"
---


<iframe src="https://trinket.io/embed/python/c424cb87eb" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>


I started out doing a grid along the x and y axes, but then I noticed that the grid lines resembled prison bars. I then decided to go with a prison theme based on my favorite tv show Oz.
I used guess and check to make the eyes look like they are in the right place. It took me a long time to make the mouth, which was just a bunch of guessing and checking. Making the tears was really difficult. I first used the stamp function to creat arrowhead-shaped tears, but I accidentally created a trail of blue behind it because I forgot to do the penup function. I thought the trail looked better. 
Later, I tried to make the pen larger, and I realized that looked much better, so I erased the stamps and just made lines of increasing width.
I wasn't sure how the tears were oriented, that is, if they are going perfectly straight down or not. I can't tell, and I would like to make it so that they face straight down. I'm sure there's an easy way to do that.
I would also like to make it look like he's behind a prison door, instead of the bars floating in nothing. 
I did the tears at the end because I thought it was a nice exclamation point ending.
Lastly, I found the hexcode for the color emerald to make the word "Oz" that color. Emerald City is the nickname for the experimental prison unit the show takes place in.

Here I am adding the tear code to see how it looks.
```
# blood teardrop on the Z
tina.goto(75,-53)
tina.color("red")
tina.pendown()
tina.pensize(2)
tina.forward(3)
tina.pensize(3)
tina.forward(3)
tina.pensize(5)
tina.forward(2)
tina.pensize(6)
tina.forward(3)
tina.pensize(8)
tina.forward(3)
tina.pensize(10)
tina.forward(3)
```
