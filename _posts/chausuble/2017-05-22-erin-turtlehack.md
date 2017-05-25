--- 
layout: post
author: chausuble
title: "Erin's Turtlehack"
---

I thought about this before going to bed one night, and I worked on this over the weekend. 
I wanted to tell a little story with the program - I decided, if you can’t erase a character, 
just have them caught up in an explosion. So, I decided to make a combat scene. I was just happy to have learned my lesson
in my basic turtle drawing to draw the background first, then draw the characters on top of it. Otherwise, the background is
drawn over the characters.

I knew it would take a lot of work - knowing that made it not very frustrating, just a lot of busywork because 
I don’t have a mind for geometry or angles, so I had to experiment with how .left and .right worked (because they are so fussy to me). 
It took a long time! My eventual solution was to use trinkets to save my code for drawing the individual shapes, 
then combining them together, and fixing the angles until the image appeared perfectly. It also helps to speed up the drawing
with tina.speed(insert number) so I can see the results right away, then slowing it down once the program was complete.
It might be also easier next time if I always fix the angles at the end of each part of the drawing - like the 
monster's head or the wizard's cloak - so the line is horizontal or vertical.

The next version will let you choose different spells to cast. For now, it just changes the color. I'd also like to see if
there's a way if the user inputs an invalid color, to ask them to re-input it. Otherwise, the program will keep trucking on
but make the color into an ominous black void. At least it still works!

Here is the program, hopefully you can also read the code if you're curious (because the whole thing is long):

<iframe src="https://trinket.io/embed/python/9abddc2520" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

I hope this gets sent to the right place!
