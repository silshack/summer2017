---
layout: post
author: samsr31
title: "Sam's Poetry Slam File Revision"
---

Here is my new, revised version of the poetry slam program, with file saving and loading added.


<iframe src="https://trinket.io/embed/python/dedf93017d" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

At first, I was pretty uncertain about this one.  I don’t feel like I’ve fully grasped how files work as well as I have previous concepts, and so I was worried this would be pretty hard.  As is, after sitting down and poking around at the problem, I was able to find out how to reliably write to a file, and then reopen that file later.  The main problem for me seems to be conceptualizing how to take a list and write it into a text file, and then how to take lines of string data from a text file and properly read them into lists.  I can do these things, but it takes a bit of trial and error to find a way that works each time.
The biggest issue for this project was not only recording a poem, but recording it’s metadata.  Since for my original poetry slam I decided to get fancy and let the user dictate the font size and text color mode of their poem, for this revision I wanted to be able to save those choices as well.  I ended up saving two bits of metadata in the final line of the poem, and then removed and interpreted that final line when the poem was opened again.
One remaining issue seems to be that you cannot open files you just saved.  Even after looping through a few other existing files or new files, any files saved during the current run of the program can’t be loaded again until the program is restarted.  I thought this might be an issue with closing the new file after writing to it, but even after including a close statement, the issue persisted.  While I’d like to figure this out, I also need to work on my blackjack program for tomorrow, so I will have to leave this problem for later.
