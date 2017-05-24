--- 
layout: post
author: chausuble
title: "Erin's Decently Functional Turtle"
---

Original: 

<iframe src="https://trinket.io/embed/python/f4e6dfc8da" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

With Functions:

<iframe src="https://trinket.io/embed/python/fd2b551c43" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>


I really needed practice writing functions, so pretty much everything that could have a function was made into one. Drawing the
background, the wizard, the monster, the spells themselves - everything! Almost all of it is similar to how it was originally.
The two that fit with the assignment are the return aspects I added to each of the spells, and how I split the "ice" spell
into three parts because of this.

Return functions: Now, at the end of each spell, I put the message that should display at the end as the Return. Here, I
discovered that if I use the Print command with a function in the parentheses, it will run the function AND print the return
message. I didn't quite get that in our homework, so for a while, I was baffled at why the spells were casting twice - I had
run the spell function once, then again through Print. Lesson learned!

Ice spell: I knew, at first, I would have to do this in at least two parts. The blizzard needed a function for the snow to fall,
then the icicles, since they are my most repetitive aspect in this program, would need to be drawn at different x and y
coordinates. So, the icicles take arguments for drawing those coordinates. All that worked out as I was hoping it would. 
The problem happened when I wanted a return message - if I put it with the blizzard, it would return the message
before the icicles appeared...but if I put it with the icicle, it would print four times because of the four icicles generated.
So, I ended up making a third function that would simply return the message I wanted displayed, then nest that in a Print
command.

Future notes: I think I might try using a function to see if I can resolve my problem with "What happens if the user types in
an unrecognized color when prompted?" It's vague right now, but my idea would be to have a function that returns whatever the
pen color is going on before the prompt begins. While in "debug" form, I can print out the return, and then go from there...
the only solution that I've really found is that you exclusively select the colors that the program will recognize for the
cloak function, or whatever the equivalent is in your program.

If I had time and we were going to work on this turtle more, I would probably redo the functions so they could work across a
lot of different situations. For example, drawing the wizard would probably take x and y coordinate arguments so I could draw
it in lots of different locations or settings. The spells would work in a similar way, perhaps also taking arguments for the
angles they would be casted, so they could strike different monsters. Finally, it's ambitious, but you could make something
like this into a game - maybe you have to select the right combination and order of spells to defeat the monster, or things
like that. For now, given the amount of time I have, I'm just happy with the light show!

You could say this exercise was..."fun"ctional
