---
layout: post
author: neatoskeeto
title: "Matt's Third Project Update"
---

Here's my program so far:

<iframe src="https://trinket.io/embed/python3/16e1d7d5ef" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

Even though I don't see as many milestones checked off as I would like, I feel like I've made a great deal of progress on this project. The first thing I worked on was to create a new class called "book" which would have all of the functions for importing and splicing the text files of the Project Gutenberg books. Once again, I used my tried and true method of printing each step as I go to make sure nothing was broken. I also decided to create a test file that was shorter than either of the two full books I uploaded, and I added "test sentences" to it to see if it calculated the most common words and sentences correctly. I got everything working right on the test file, so I tried it out on the full books, but it was causing an error on the H.L. Mencken book. It turned out I had to add a space to one of the lines in the file to make my program read it properly. The calculations for word count take quite a while, so I used Aaron's "print processing" function from his printer module to show that the application hadn't crashed. I plan to do something else 
```
#Copied from Aaron Plocharczyk <https://silshack.github.io/summer2017/businessowl-project-update-stand-up-2.html>

def print_processing():
  print("Working on it...")
  time.sleep(1)
```  
I am still confident that I can accomplish my goals, because the base caulculations are done. I need to visualize the statistics in a histogram, create a loop that allows for the user to compare several books at once. And display the most common words for each book.
My milestones are the same as before. I feel I can accomplish them in time:
<ul>
 <li>[X]   Read Project Gutenberg text file.</li>
 <li>[X]   Isolate the relevant text from the file.</li>
 <li>[X]   Calculate average word, sentence, paragraph lengths</li>
 <li>[X]   Store these statistics for comparison to other files. </li>
 <li>[ ]   Visualize the data with histograms.</li>
 <li>[ ]   Save the statistics in a new file.</li>
</ul> 

Advanced milestones:
<ul>
  <li>[ ]  Add abilitiy to enter a URL to store a new Project Gutenberg book into the program and perform the same analysis.</li>
</ul> 
