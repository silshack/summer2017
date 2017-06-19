---
layout: post
author: nvola
title: "Natasha's Project Update 3"
---
Here is my most recent trinket for my final project:

<iframe src="https://trinket.io/embed/python3/ff1d8eb0cd" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>


Since my last update I was able to add in some data visualization. I decided to go with a graph of the whole series of data based on the region the user input using the matplot module. This was a little difficult to figure out because the documentation for matplot doesn't do a great job of actually explaining what each method/function does in matplot. Since the data is over time, it didn't seem informative to only map out the two points of time being pulled for the percent change analysis. Similarly it didn't really make sense to visualize the descriptive stats data any other way that just presenting the whole thing; so that's why I decided to visualize the data the way I did. I was able to get it to graph everything based on user input by using for loops.


Looking ahead, I want to try to incorporate some of the regular expressions to allow a little flexibility on user input, but I'm thinking that I won't be allowing too much flexibility since 1) the program needs to be able to run without too many errors and by pulling the right data (which might be impeded to making it too flexible to user input) and 2) in theory, a user could and probably should clean their dataset prior to running it through any kind of analysis tool. I'd like to attempt the stretch goal of computing the intervening times for the percent change analysis, but I think that would require a lot more time than I currently have to map out the for loops that would be required to make it possible. 


Here's my updated milestone list. I realized that I needed to remove the items related to analysis three since I ended up merging that with analysis 2, so those are the only changes to the milestones:

Already achieved
- [x] read user file (csv format)
- [x] read headers in user file
- [x] pull relevant variable based on user input (based on file headerss)
- [x] create menu for 3 analysis options
- [x] create analysis one skeleton code
- [x] menu/user instructions
- [x] accept user input for necessary information
- [x] present available regions from data
- [x] present available years from data
 
To be achieved by Wednesday: 
- [x] present available variables from data
- [x] create analysis two skeleton code
- [x] ~~create analysis three skeleton code~~
 
To be achieved by Monday:
- [x] create visualization for analysis one
  
To be achieved by Tuesday:
- [X] create visualization for analysis two
- [ ] ~~create visualization for analysis three~~
- [ ] incorporate regular expressions to allow flexibility on user input
 
Stretch goals:
- [x] implement capability to do multi-region analysis for percent change
- [x] make the descriptive statitics analysis flexible to compute either one region or multiple regions so it can be one menu option
- [ ] allow percent change (analysis one) to be computed at the intervening intervals between the user's chosen end and start date
