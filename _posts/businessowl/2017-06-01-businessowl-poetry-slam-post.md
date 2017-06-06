---
layout: post
author: businessowl
title: "Aaron Plocharczyk's Poetry Slam"
---

<strong>Here's the program I'm embedding:</strong>

    <iframe src="https://trinket.io/embed/python/edbd7c0357" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>
    
<br/>
<strong>Reflection:</strong>
<br/>
The first thing I did was collect user input. I used a while True loop to do this and exited the loop when the user input was "done". I stored all the lines as items in a list. Then, I made an invisible turtle that would loop through the length of the list and write each line to the screen. This overlayed all the lines on top of each other, so I added a goto(x, y) withing that for loop so I could pick where I wanted each line to be written. I had to make the y coordinate increase each time a line was written, so I decided to base the y coordinate on the current index of the for loop. This worked well, but I had to offset the y coordinate by 200 so it would center on the screen instead of just writing on the lower half of the screen. Ultimately, the formula I ended up with for my y coordinate was (-20 * currentIndex + len(lines) * 10). That seemed to work well.
<br/>
After all that, I wanted to make the program stop the lines from overflowing off the screen horizontally if a user entered a line that was too long. To do this, I first determined which letter of the alphabet was the widest by typing all 26 of them out on separate lines, 10 times each. It turns out that capital "M" is the widest. Then I wrote a tone of M's on the screen to see how many the screen could hold. It could hold 33 of them. So while I was accepting user input, i made it so that if a user entered a line that was more than 33 characters long, it spearated it out into multiple list items, each with a maximum length of 33 characters.
<br/>
As a final touch, I made the screen's background dark gray and made the lines white, so it had a slam poetry feel.
