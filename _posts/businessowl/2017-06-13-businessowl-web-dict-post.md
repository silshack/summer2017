---
layout: post
author: businessowl
title: "Aaron Plocharczyk's Web Dict Post"
---

<strong>Here's the program:</strong>
<iframe src="https://trinket.io/embed/python3/d998f2bd18" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>
    
<br/>
<strong>Reflection:</strong>
<br/>
The first thing I did was choose which pieces of data were most important. I went with location type, formal address, longitude, and latitude. Location type will say things like: "Approximate" if the address is not exact, "Rooftop" if it's able to narrow the location down to a specific building, etc...
<br/>
After that, I put that info into a list of lists so I could format it like a table. Then I noticed that if I was going to use a table, I could add more than one result (should the search ever yeild more than one result). <strong>You can search for "there" to get multiple results and check this out.</strong> So I added a loop to go through all the results, construct a list for that result, and add that list to the list of lists.
<br/>
From there, I stole some code from my CSV assignment that I wrote to print a nicely formatted table, given a list of lists as a parameter. Using this, I could print out the data from all of my results as a table, but the addresses often overflowed the max allowed space for their cells, so I had to fix that. To fix that, I had to write a function to wrap the text in a cell so it doesn't overflow. this function is defined as follows:
```
def text_wrap_last_row(subtable, col_width):
  while len(str(subtable[len(subtable) - 1][0])) > col_width or len(str(subtable[len(subtable) - 1][1])) > col_width or len(str(subtable[len(subtable) - 1][2])) > col_width or len(str(subtable[len(subtable) - 1][3])) > col_width:
      list_to_add = []
      for i in range(4):
        if len(str(subtable[len(subtable) - 1][i])) > col_width:
          list_to_add.append(str(subtable[len(subtable) - 1][i])[col_width:])
          subtable[len(subtable) - 1][i] = str(subtable[len(subtable) - 1][i])[:col_width]
        else:
          list_to_add.append("")
      subtable.append(list_to_add)
  return subtable
```
Really, what it does is take any values that are longer than the max allowed character length and put the extra parts of them on a whole new line (i.e. keeps the first n characters in the current list and appends another list with the excess characters until all lists are acceptable). My final step was to do error checking. For this, I added try and except clauses around the each line where I access the value that I am trying to get. If the data does not exist, an exception will be thrown, and when that exception is caught, it will just substitute "N/A" for that data and continue with the program.
