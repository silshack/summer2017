+---
 +layout: post
 +author: nurahill
 +title: "Nura's Drawing App"
 +---


Drawing App Milestones: 

- [ ] Make a cool Design
- [x] Give user option to click or use the keyboard
- [x] Give user control of turtle color and background color
- [x] Give user control to draw a few shapes
- [x] Design a legend for keys
- [ ] Design a legend for arrows


Here is my embeded code: 
<iframe src="https://trinket.io/embed/python/0d68bfd55e" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

When the clicky turtle assignment was due, I did a basic drawing turtle, which was the basis of what I have done for this drawing app assignment. Because I don’t feel one hundred percent confident with coding yet, It did take me a long time to put everything together. I think that If I had more time to focus on this, I could make it a lot better than what it is now, design wise at least. Therefore, I don’t feel like I completed a successful design milestone. I was able to figure out how to do have the user be able to use both the keyboard and mouse to make it do different things. Ex: If you press “s” it draws a star, if you press “u” you can penup/pendown, if you “x” you can clear the screen, if you press “shift” you can change color of turtle, and if you press “b” you can change the background color. Those are the milestones I feel like I successfully completed. I intended to add more shapes, but I just spent to much time doing other things to get to it to work, so I decided to just give the user the ability to draw the star. I wanted to make a cool legend, and I decided to draw it in another program and then insert it into the code as an image, however, I was not able to figure it out. 
```
screen = turtle.Screen()
screen.bgcolor("medium spring green")
image = "lengend.gif"
screen.bgpic("legend.gif")
screen.addshape("image")
```
As you can see above, I have a bg color set, then I add the image, but for some reason I am not able to leave the image on the screen the whole time and have the background color change. Meaning that when the user tries to change the background screen, it will completely take off the lengend. So that milestone kind of failed. I also wanted to have another small legend on the bottom corner of the screen that showed arrows, but because I was having such an issue with the first legend, I decided not to do that one. 








