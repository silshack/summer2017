---
layout: post
author: jpanken
title: "Jaffa's Rock, Paper, Scissors...Click!"
---

Here's my version of Rock, Paper, Scissors:
<iframe src="https://trinket.io/embed/python/8bba1488bb" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>


There is a lot of code in this that could probably be condensed.  I wasn't exactly sure how to migrate turtles that I created in helper.py into main.py.  I think that I needed to set those turtles as global, but I decided that it wasn't that important.  Also, I wanted the player to choose their instrument simply by clicking, but it kept on reverting to Paper.  

It took me a long time to figure out that I needed to define player_score and comp_score outside of all the while loops so that the score wouldn't reset to 0 before every new game.  For the future, I'd like to work on the clicking thing, figure out how to limit the games played to 3 (I could probably use a for loop), and make it spiffier.  Enjoy!
