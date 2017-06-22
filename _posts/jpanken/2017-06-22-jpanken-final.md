---
layout: post
author: jpanken
title: "Jaffa's Final Project"
---

<iframe src="https://trinket.io/embed/python3/248549c26a" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>


This is it: a data analysis program on Kickstarter projects.  I started this project thinking that I would scrape tweets, but I couldn’t decide what to scrape.  Instead, I went looking for datasets and found one about foreign and domestic Kickstarter projects on Kaggle.  Once I cleaned the data and started figuring out what sorts of things I could do with it, I decided that it wasn’t enough.  Instead I found another dataset that compared successful and failed Kickstarter projects.  I though that this was a much stronger basis for comparison so I downloaded the data and prepared it to be uploaded into my project.


After the data was ready, I had to figure out how to organize the menu options and data visualizations.  I procrastinated on this for awhile and set to work on the dictionary.  I decided early on that I could best fulfill this requirement with a help dictionary.  I was thinking that the user needed to know where the data came from and what it meant.  So I compiled a single dictionary that can be used for all the help functions.  Each value is worded so that it can be inserted into a given format and make sense to a user.  I only made one dictionary, but made certain keys accessible from certain menu options to keep everything clear.


I had a little snafu with the dictionary because it returned a value even if you enter an invalid key.  For that reason, I was initially unable to use a function for returning the answer.  In my update, I reached out to my group members asking for advice.  Zach helped me out and developed a snapshot of a function to streamline the help code, however this code threw an error if the user typed in a bad number.  At first I thought that I would use a try-except sequence, but I had trouble getting that to work.  Instead, I reconfigured Zach's suggestions into an if-elif-else statement within the function to inform the user that s/he had typed an incorrect number. Problem solving strategy #1: Ask for help from your peer group. 


When I came back to work on the options menu, I was able to think about it more clearly.  This illustrates a problem-solving strategy that I seldom used during the fast-paced semester: taking time away from the problem. While I wasn’t actively working on the issue, I was passively thinking about it.  This led me to reconceptualize the arrangement of the options menu.  Instead of making users choose the type of data first and then the visualization format, I decided that to reverse my approach.  Since you can only do certain things with certain data types, I was able to present more choices by giving them the visualization options first.


Throughout the semester, I have struggled to use custom modules and functions.  After the mini-lecture on modules, I was able to incorporate some of that information into my program.  First, I tried not to clog up the name space except when absolutely necessary.  This required some reconfiguring to incorporate the module names when I called the functions.  I had also learned a lot during the Blackjack assignment, but it hadn’t totally sunk in until later.  This allowed me to design the functions from the beginning rather than retrofitting long-winded code. 


I first created a variables module to allow the program to create new lists over and over again depending on the dataset that the user had chosen.  Then, I made a functions module to keep all of the functions that would be called over and over again.  After that, I worked on the dictionary module as discussed above.  Finally, I decided to make a user interface module to keep all the options menus and any interactions with the user.  This module ended up keeping the vast majority of the code as I set up the scaffolding for the program in this module.  All of the various options are defined in the user interface and a series of if-elif-else statements. 


Each if-elif-else allows the user to input the number that aligns with their choice and then executes the functions kept in the functions module.  I decided that the user should only have to type in numbers because there are too many ways that words can go wrong.  The user could have the caps lock on, or misspell a work, or just get confused.  If the user does type in a bad number, the program will print out an error message and return to the Main Menu.  In that way, the program is very unforgiving.  I do wish that it would just return to the previous menu, but I couldn’t figure out how to make that happen as I would have to structure the options in a series of while loops and I don’t know of any way to switch between while loops all willy-nilly.


Another one of my priorities was making the program dialogue easy to read.  At first, I thought it was sufficient to line up the various options and just let the user stream through the program.  Then I realized that it might be useful for the user to know whether s/he was looking at options or information.  I decided to separate the input from the output with a function called ‘get_divide’.  I had a little bit of confusion about where to place my ‘get_divide’ statements so that they were where they needed to be and not doubled because they were in multiple aligning functions.  That took a lot of testing.


After I had the ‘get_divide’ statements in, I realized that they broke the flow of the program so much that users might forget what they were looking at.  This issue was compounded by the number inputs so that the user could not just look back at their last input to remember.  So I created a statement called ‘get_title’ which was derived from the dataset file name.  Originally, there were two titles available, “Successful Kickstarter Projects” and “Failed Kickstarter Projects.”  Later, I realized that I needed to also have titles to label each of the program outputs.  I decided to combine the expanded titles with the ‘get_divide’ function into a class called ‘Style’.  I played with various characters for combining the divisions with the titles.  I had a rather sophisticated system for ascertaining how many snowflakes are necessary to offset the title lengths: trial-and-error.


Trial-and-error has been my main problem-solving strategy throughout this course.  I am constantly monitoring if the changes I made had the intended effects and whether I need to make further adjustments.  Part of that process is printing out various statements to check the flow of my program.  I did not do as much printing as I normally do while developing programs, most likely because this was a text-based application that had a lot of printing already.  I was, therefore, able to see exactly where things went off the rails without putting in fail safes.  


Over the course of my project, my milestones did not change very much.  I ended up working on my program in a few concentrated increments and mulled over how to make things work in the interim.  This is not to say that my project did not evolve, but my milestones were very general.  As a result, I did not lock myself into one way of solving the problems that emerged.  I preferred this approach to having a grand scheme that I would inevitably fail to execute.  That said, there was a milestone that I never articulated, but failed to accomplish.  I had hope to write the results to a file, but I was never able to figure out how exactly that would work with multiple datasets.  I’m willing to admit that I didn’t work very hard to make that happen as I was quite focused on how to present the data.  


I did, however, manage to put together a data analysis program with a minimum of fuss and panic.  This is a world away from where I started this course, staying up half the night in an attempt to make turtles appear where I clicked.  At the beginning of this course, I struggled with knowing where to start and very basic planning.  Now, I have created a program that takes extensive data files and spits out information about their content.  As far as I am concerned, that is an accomplishment of which I can be proud.


### Milestones
- [x] Import clean data files into program
- [x] Compile each column in list for ease of use
- [x] Offer a help dictionary in all of the options menus
- [x] Provide additional information about datasets and types of data
- [x] Present help menu in an elegant way
- [x] Keep user interface and output organized (with a class)
- [x] Options menus with 2-3 layers
- [x] Divide data into logical subsets for the options menus
- [x] Manage errors
- [x] Provide different formats for data visualization
