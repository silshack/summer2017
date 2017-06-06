---
layout: post
author: zman7895
title: "zman7895's poetry slammmm!"
---

Below is my embedded poetry slam trinket.

<iframe src="https://trinket.io/embed/python/6ca4bde42a" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>


I first just did the basics of creating a background color, a turtle, and setting the turtle to the color I wanted as well. Then, the first thing I did was send the turtle to the upper right of the screen where I would want to start the poetry. My first guess was pretty accurate so that didn't take too long. I began by simply running a loop that would consistently ask the user for input and having the turtle write it. However, I quickly realized that when it wrote, the turtle wouldn't move, so when it went to write again, it would simply write over it. That is when I learned I needed to move tina after each input. I decided to set it up so tina would go to a new location after each input, and I used her current coordinates and moved it down to the next line based on that. That was my first challenge.


The next challenge was dealing with too long of lines. By trial and error I figured out how long a string would have to be to exit the screen. Once I realized it was about 40 characters, I decided to set up logic that would splice the string if it went over 40 characters, and move the spliced string down onto the next line. I implemented this logic for entries that would span up to three lines. If the user enters more than three lines, I ask the user to write shorter lines.


Lastly, I wanted it so they couldn't go over the page. I learned there was 16 lines they could use. I implemented a linecount variable and increased it everytime they entered a new line. If they entered one line it would increase count by 1, if they entered 2, it would increase 2, etc. Then I added the logic that if the linecount hit 16, it would tell the user to save their work and start again on a new slate. I would like to know if there was a way to adjust the screen and move it down, or if I could shift the words up and have them keep writing, or lastly, if I could have cleared the screen but saved it at the same time. These would all be changes or additions that would make my slam better if I had more time. 
