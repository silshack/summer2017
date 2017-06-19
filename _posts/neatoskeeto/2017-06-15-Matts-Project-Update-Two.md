---
layout: post
author: neatoskeeto
title: "Matt's Second Project Update"
---

Duplicate trinket:
<iframe src="https://trinket.io/embed/python3/ac2a6c6b68" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

I feel like I've made quite a bit of progress. I decided to revise the scope of my program so that it only analyzes text files from Project Gutenberg. I then uploaded two sample files from Project Gutenberg and stored them as modules in the trinket. My next task was to make code that isolates just the text of the book and not the metadata from the beginning and end of the text files. My first instinct was to split the string on every instance of the title, because the title appears at the beginning of the book and in an ending string in the format "*** END OF[TITLE] *** However, because the titles are formatted differently in different books (one is all caps, the other just initial caps) this wasn't working. I first fixed this by capitalizing everything in the file, but I didn't like how it looked. Ultimately, I decided to isolate the string between "*** BEGINING OF [Title] ***" and "*** END OF [Title] ***"  However, because one of the files does not have a space between the asterisks and the words, the find method didn't work, so I "cleaned up" the data by standardizing the spacing there.

My next task is to isolate the sentences, paragraphs, and words so I can measure their lengths and average them out and visualize the data.

```
 start_of_book = book_raw.find("*** START OF")
  print(start_of_book)
  end_of_book = book_raw.rfind("*** END OF", 0, len(book_raw)-1)
  #print(end_of_book)
  
  #this should remove all text except for the actual book
  book_block = book_raw[start_of_book: end_of_book]
  #print(book_block)
  
  paragraphs = book_block.split("\n\n")
```
Because the end of each line is not necessarily the end of a paragraph or even a sentence, I decided to isolate the paragraphs by splitting on double line breaks. That seems to work well.

I have a weird issue where before apostrophes, the data prints out a '\', and I'm not yet sure if that will affect the word lenghts or not in any significant way.

My modified goals are as follows:

 [X]   Read Project Gutenberg text file.
 [X]   Isolate the relevant text from the file.
 [ ]   Calculate average word, sentence, paragraph lengths
 [ ]   Store these statistics for comparison to other files. 
 [ ]   Visualize the data with histograms.
 [ ]   Save the statistics in a new file.

Advanced milestones:

  [ ]  Add abilitiy to enter a URL to store a new Project Gutenberg book into the program and perform the same analysis
