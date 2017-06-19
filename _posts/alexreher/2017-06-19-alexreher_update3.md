---
layout: post
author: alexreher
title: "alexreher project update 3"
---

Current snapshot: <iframe src="https://trinket.io/embed/python3/242c7943a5" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

###Old Milestones
 - [x] Get data sample for textbooks
 - [x] File ingest
 - [x] Parse Call number ranges
 - [x] Make callnum dictionary
 - [ ] Make the menu
 - [ ] Instantiate classes for shelves
 - [ ] Add counts
 - [ ] Add help function 
 - [ ] Add LoC dict to help function
 - [ ] Display active range selection on menu
 - [ ] Variable shelf options
 - [ ] Range as percent of whole
 - [x] branch selection
 - [ ] Max from regions
 - [ ] Avg/Min from regions
 - [ ] Ask user min/max/avg

###New Milestones
 - [x] Get data sample for textbooks
 - [x] File ingest
 - [x] Parse Call number ranges
 - [x] Make callnum dictionary
 - [x] Make the menu
 - [x] Add other file ingest options
 - [x] Instantiate classes for shelves
 - [x] Build visual for the shelf
 - [x] Add range/collection counts
 - [ ] Add help function 
 - [ ] Add LoC dict to help function
 - [ ] Display shelves based on input
 - [ ] Have Shelf density reflected visually
 - [ ] Display active range selection on menu
 - [x] Variable shelf options
 - [ ] Range as percent of whole
 - [x] branch selection
 - [ ] Library comparisons
 - [ ] Max from regions
 - [ ] Avg/Min from regions
 - [ ] Ask user min/max/avg
 - [ ] Update menu to reflect full range of options

I'm really happy with the back-end of my program. I think I've modularized it(sounds like a verb) really well. There are a few global variables, but for the most part, action takes place in very specific functions and modules. This means that while I have a bunch of milestones left, they are, for the most part, smaller. As I've made some progress, I broke up some of what were bigger milestones into the more manageable pieces I ended up tackling. Breaking these pieces down was a big part of making the project approachable and ensuring that I'd occasionally get the little boost from achieving some minor goal.

There's some stuff I'd like to implement as stretches, but they all require a bit more time than I might have. I think knowing what I wanted the program to be able to do without time constraints helped me shape it so that I'll be able to add functionality without having to generate much more code. Adding visual representation of shelf density might be tricky, but I'd really like to have it work.

My planning initially wasn't great, waiting too long for the ideal data forced me to change plans. With the change I didn't have as much of a vision for my project. Having some time off before the weekend gave me a chance to ruminate on things and come up with the shelving density concept that's much more visually interesting than a table of numbers. It also helped me make sure I went into the weekend with specific tasks in mind.

I have the functions and data parsing I need, so my next step is just to combine my little componenents in all the ways that can give the users some statistics and visuals for them. By the end of today I'd like to have the basic shelf output visualization working so that I can move onto the help feature and finally some stretch goals.
