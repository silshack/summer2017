--- 
layout: post
author: chausuble
title: "Erin's Poetry Turtle with Files"
---

<iframe src="https://trinket.io/embed/python/436dda692a" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

It looked easy in theory, but for some reason, it doesn't actually save the written poem! It just saves something called
[object Object] for every line of the poem, and there wasn't anything I could find online that would help me. If I'm lucky
I'll figure it out before class, but if not, this is what I have. Again, in theory, if you loaded a poem, it would write each 
line of the poem on the screen, and print it, too. If you saved a poem, it would save the poem list to the file, so the
program could re-read it like it usually does for other poems.

Here's the code where I think the problem is. This one is to open the file:

```
open_old_file = raw_input("Would you like to open an old file? y/n")
if open_old_file == "y":
  file_name = raw_input("Type the name of the file you want to open.")
  file_name = open(file_name)
  file_name = file_name.readlines()
  tina.goto(changex, changey)
  for each_line in range(len(file_name)):
    tina.write(file_name[each_line], None, "left", ("Arial", "18", "normal"))
    changey = changey - 22
    tina.sety(changey)
    print(file_name[each_line])
```

This one is to save a new file:

```
save_poem = raw_input("Would you like to save your work? y/n")
if save_poem == "y":
  save_file_name = raw_input("Name your file...")
  save_file_name = save_file_name
  save_the_file = open(save_file_name, "w")
  save_the_file = save_the_file.write(poem_list)
```
ETA: I reread our old exercises and realized I forgot about the .join function! So as it turns out, my solution was to change the save file like this:

```
save_poem = raw_input("Would you like to save your work? y/n")
if save_poem == "y":
  save_file_name = raw_input("Name your file...")
  save_file_name = save_file_name
  save_the_file = open(save_file_name, "w")
  poem_strings = "\n".join(poem_list)
  save_the_file = save_the_file.write(poem_strings)
```

So the idea I had to convert the list into strings was on the right track. I just had to remember that at the end of each list item, have a "\n" to break them into poem lines. Now I think it's working. I don't know why this idea only came once I submitted the assignment. I won't question it.
