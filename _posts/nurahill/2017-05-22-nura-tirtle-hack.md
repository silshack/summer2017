---
layout: post
author: nurahill
title: "Nura's Turtle Exercise"
---

Here is the program i am embeding:
 <iframe src="https://trinket.io/embed/python/0af7db0563" width="100%" height="356" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>
 
 This assignment was fun. Just like the first one. When I started the assignment I had no idea what i wanted to do. So i googled things for inspiration. I did not know that we had to cite where we got code from if we used someone elses code, but i will do my best to find and it add it somewhere. So basically what I designed was a logo (because thats kind of what it looks like). See image below.
 
 ![Turtle image](https://trinket-user-assets.trinket.io/766ef1ddb2e8fcf44c2522a82c38d12138860fcb-59239d72d1f91c5f706e1ad2.png)
 
 Online I found that I could do a start, cool/weird looking circles, and interesting patterns. So what i did was take all of these things and merge them together and place them where I wanted them to go in order to have a ok looking design. I really struggled when I was playing around with the dots. The original dot patern had like 5 dots across and 7 down. I wanted to change that to make it go on the whole screen. After a lot of trial and error, I was able to expand it and make it go across the whole bottom half of the screen. I noticed when i was playing around with it that i could only fill the screen by quarters, so that meant that i had to copy/paste the code (from line 23-32) and change what was backwards to forwards and was left to right, etc. 
 ```
 #Dots
ninja.color("turquoise")
dot_distance = 25
width = 10
height = 10
ninja.penup()
for y in range(height):
    for i in range(width):
        ninja.dot()
        ninja.forward(dot_distance)
    ninja.backward(dot_distance * width)
    ninja.right(90)
    ninja.forward(dot_distance)
    ninja.left(90)
turtle.done()
ninja.goto(0,0)

for y in range(height):
    for i in range(width):
        ninja.dot()
        ninja.backward(dot_distance)
    ninja.forward(dot_distance * width)
    ninja.left(90)
    ninja.backward(dot_distance)
    ninja.right(90)
    ```
 When it comes to the stars and the sun, I took a good while to try and figure out where to place them. The stars were originally just outlines and i filled them up with color. The sun originally had a different shape, I messed around with the range, and the other numbers to give it a different look. 
