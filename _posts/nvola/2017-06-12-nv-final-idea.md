---
layout: post
author: nvola
title: "Natasha's Final Project Idea & Work Plan"
---

I've already began work on my final and have already achieved a lot (I think). 

<iframe src="https://trinket.io/embed/python3/1625605930" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>


My initial milestones include:
- [x] read user file (csv format)
- [x] read headers in user file
- [x] pull relevant variable based on user input (based on file headerss)
- [] permit 3 types of analysis (percent change, descriptive stats for 1 region, descriptive stats for multiple regions)
- [x] menu/user instructions
- [] present text-based data visualization
- [] accept user input for necessary information

In my job we look at a lot at change over years of data, and I hate calculating it manually, so I knew that I wanted to include that as an analysis with this program. I also want my program to be flexible enough such that any type of data could serve as input for the program as long as the data has a header for region and a header for year, which I think I've mostly achieved. I'm passionate about public health so the test data I'm currently working with is all health-related from the WHO (maternal death rates and life expectancies for women, I didn't intentially choose two super depressing datasets, that just happened), but, as I've said, I think that this program could work with other datasets as well. I still need to work on creating custom classes, figuring out an error issue with one of my analyses, and working out the third analysis. One of the things I'd like to incorporate if I have time is some regular expressions such that the case of the headers doesn't matter (I had to manually make the cases match with my current test data), and such that the user doesn't have to produce an exact match for their inputs (currently they have to). 

Thinking ahead, these would be some additional milestones I'd like to or need to achieve:
- [] custom classes
- [] allow seamless multi-region analysis
- [] allow percent change at intervals between the chosen dates, if the data exists
- [] incorporate regex to allow user flexibility on input


A challenge I've encountered so far is that I tried separating the code out into some modules, but they're all kind of passing variables between one another so the links between them is messy. Another thing is working with dictionaries, because I'm still a little confused about aspects of dictionaries. 
