---
layout: post
author: businessowl
title: "Aaron Plocharczyk's slam poetry files post"
---
<strong>Here's the trinket:</strong>
  <iframe src="https://trinket.io/embed/python/e1f47da4c8" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>
<br/>
<br/>
<strong>Reflection (which is not actually required, per the instructions?):</strong>
<br/>
I gave the user the ability to save their lines to a file and reopen them later if so desired. I don't allow the user to name the file nothing (i.e. "") because that doesn't seem to work when reopening the file later. Everytime you give an input, the program checks your input for validity and reprompts you if it turns out that the input was invalid. I did this with while loops and try/except clauses. It seems like the directory doesn't update with new files until you stop the program, so you cannot open files that you just created until you stop the program. I make sure the user knows this right after they create a new file by printing the message: "File saved! YOU NEED TO RESTART THE PROGRAM BEFORE REOPENING THIS FILE.". It would be nice to learn about a workaround for this. I tried some things that I found online but nothing worked.
