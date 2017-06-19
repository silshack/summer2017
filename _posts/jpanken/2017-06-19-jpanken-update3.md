---
layout: posts
author: jpanken
title: "Jaffa's Third Project Update"
---

<iframe src="https://trinket.io/embed/python3/8f440f55a1" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>


I basically finished the program this weekend.  I was able to reconfigure the menus to choose first between different datasets, then different presentations of the data, and finally different types of data.  Most of my program is housed in user_interface.py through a series of functions.  The first option menu, however, had to be in main.py because otherwise the user was unable to switch between different datasets during the same session.  Each of the other options are nested functions within the second options menu.  I had to work on each function one by one because I kept on losing my place.  


I still haven’t employed a class for formatting purposes.  That will be my next task.  I also hope to further clean up my code and make it readable.  Otherwise, I will focus on helping my groupmates.  While he was sick, Zach played with my code and was able to use a function to shorten the help dictionary.  While I eventually rewrote the code so that it didn’t throw an error when I typed in an invalid number, Zach set an excellent example for how groupmates should support each other.  This is an example that I hope to follow.


### Milestones
- [x] Import clean data files into program
- [x] Compile each column in list for ease of use
- [x] Offer a help dictionary in all of the options menus
- [x] Provide additional information about datasets and types of data
- [x] Present help menu in an elegant way
- [ ] Create a class Style to keep user interface and output organized
- [x] Options menus with 2-3 layers
- [x] Divide data into logical subsets for the options menus
- [x] Develop error management
- [x] Settle on format for data visualization
