--- 
layout: post
author: chausuble
title: "Erin's Logical Turtle"
---
Here is my updated turtle:

<iframe src="https://trinket.io/embed/python/f4e6dfc8da" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

My goal with logical statements was that it would ask the user for one of three spells. If you type in one of the three,
then it casts the spell. If you make a typo or make up a new spell, it gives an error. That seems to have worked out fine,
but the other aspect is when I did a "try" and "except" for the cloak color. I thought that if I put in a typo for the
color or typed one that didn't exist, it would come up with an error. Instead, it just keeps drawing the cloak...but
it's pitch-black! I mentioned this last time, and I thought a try/except would avoid that. I guess, however, it's nice
that the program still works! I don't know what causes that - is it something about the Turtle function itself?

Anyway, after working in groups yesterday, I saw some neat tricks that I wanted to factor into my
updated turtle. I got to achieve my goal of letting the user pick out spells they wanted
to cast. Jaffa’s had some cool effects on display. In particular, I used the changing backgrounds
for the lightening spell. She also linked a website that shows off different effects you can do with turtle that 
I would never have dreamed of, so I might experiment with those to see what happens.

Again, I’ve found that when I have a lot of working parts to a program - so many drawings and so many angles - 
it helps to make many smaller trinkets with each “drawing” programmed in. That way, I can assemble them together 
part-by-part, and fix the angles until the pictures look they way I want to - or close enough! For me, it made things 
a lot less frustrating than seeing a huge wall of code - less intimidating to start by drawing a line, then changing 
the angle of the line, then drawing the next line, little by little. Before I knew it, I had all the different spells 
ready to put together.

Since I struggled with this, I’ll put notes for it - when it comes to having the background change the way I did, 
where I wanted to cycle through different colors, the turtle cursor has to be doing something. You can’t just order 
the background to change - otherwise it just instantly changes to the last color on the list rather than going 
through all of the colors. I did this just by having the cursor turn right and left at equal angles so it was back
to its starting position.

```
  for i in range(1):
    tina.speed(1)
    myscreen.bgcolor("skyblue")
    tina.right(10)
    myscreen.bgcolor("lightgray")
    tina.left(10)
    myscreen.bgcolor("darkgray")
    tina.right(10)
    myscreen.bgcolor("gray")
```

Again, this is thanks to Jaffa's turtle: https://trinket.io/embed/python/fb814f79b7

If I were to keep fixing this, I would like to make sure the fire’s angles are lined up right. I would
also like to use some curved lines, like what's used in neatoskeato's cool turtle at 
https://trinket.io/embed/python/c424cb87eb, to help draw the wizard and monster’s bodies. 
Skimming at what functions do, I think it would be cool to further update
the spell-casting system. My friend showed me some old programs on the Internet Archive,
where some old video games would have you select ingredients for a spell and then you could
cast them - you could do something where the user types in two ingredients, 
and then the combination creates a particular spell. I think that will take a lot of time for what I have right now.
Instead, maybe I can have a function to help draw the characters or special effects, 
or one that has the user input how big they want a spell to be, and changing the size of the spell to reflect that.
