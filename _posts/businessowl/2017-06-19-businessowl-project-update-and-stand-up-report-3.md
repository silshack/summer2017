---
layout: post
author: businessowl
title: "Aaron Plocharczyk's project update and stand up 3 post"
---
<strong>Here's the current trinket:</strong>
<iframe src="https://trinket.io/embed/python/87a8598280" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

<br/>
<br/>
<strong>Progress since last class:</strong>
<br/>
I spent the weekend flying out to be a groomsman in a wedding, but I still got some things completed for this update. Firstly, I keep track of the all the results from testing on a particular file, which is very useful. When you test on a file, you want to compare your results with previous tests on that file to see how much you have improved. I made it so that when you test on a file, it only shows results from previous tests on that particular file, because results from other files are not relavant. Additionally, I visualized these results by printing a bar graph of the results every time you test. This makes it really easy to compare your currently perfermance to previous performances. This brought me to the end of my regular goals. From there, I met one of my stretch goals, which was to have the program give a solid introduction to itself when it starts running. This introduction makes sure the user can figure out the gist of what the program does before they explore the commands that are at their disposal. I also added the ability to type "exit" to terminate the program, and I added the ability to the program to handle training/testing files that are improperly formatted. I have been working ahead so much on this project because I knew I'd have a lot of work to do this week for my job, but for the final version of my project, I will also add comments to my program to make it more easily readable. Additionally, I'll see if I can find time to allow the user to revert back to the selection table that has given them the best results.
<br/>
<br/>
<strong>OLD Milestones:</strong>
<br/>
By 6/14:
- [x] program asks user for a training file and creates a "trainingFile" object from it
- [x] program can print two dimensional list structures as well formatted tables
<br/>
<br/>
By 6/15:
- [x] program counts total number of occurrences for each term
- [x] program counts total number of occurrences for a specified term
- [x] program calculates correlation of terms with a sentiment
- [x] program calculates correlation of a specified term with a sentiment
- [x] program allows user to perform any action with a the training set at any time by letting them type their own commands
<br/>
<br/>
By 6/19:
- [x] from the moment the training file loads, the program maintains a current "selection" of terms from the training file that the user wants to consider, defaulting to all of them
- [x] program allows user to view this selection table at any time
- [x] program allows users to specifically select or deselect certain terms
- [x] program allows user to specify upper and/or lower <i>numer-of-occurrences</i> thresholds that will automatically deselect any terms not between those bounds
- [x] program allows user to update those thresholds at any given time
- [x] program allows user to view "deselection" table at any time, which includes a reason for deselection
- [x] program allows user to "focus on" (meaning: view the state of) a specified term at any given time
- [x] program includes the following information in all of these tables: Term, Polarity, Count (# occurrences), Correlation with each sentiment, and Selection Status (and if deselected, how it was deselected. i.e. "deselected", "< threshold", or "> threshold")
- [x] user can sort any table they are about to print by any of its columns
<br/>
<br/>
By 6/22:
- [x] program asks user for a testing file and creates a "testingFile" object from it
- [x] program tests current model on the test file and prints the results
- [ ] program saves the results locally to refer to in the next iteration of the program
- [ ] program prints a visual representation of the test results as compared to previous tests
- [x] program allows user to type "help" at any time to learn about what they should do
- [x] program allows user to get further details about the commands listed in the help menu (implemented programmatically although the details aren't well articulated right now)
- [ ] program repeats
<br/>
<br/>
Stretch Goals:
- [ ] program keeps track of the most accurate model you have built so far
- [ ] program allows the user to visualize a column of the last table they printed
- [ ] program allows user to save model in a comma separated format
- [ ] program allows user to open saved models
- [ ] program allows user to alter saved models
- [ ] program allows user to test with saved models

<br/>
<br/>
<br/>
<strong>CURRENT Milestones:</strong>
<br/>
By 6/14:
- [x] program asks user for a training file and creates a "trainingFile" object from it
- [x] program can print two dimensional list structures as well formatted tables
<br/>
<br/>
By 6/15:
- [x] program counts total number of occurrences for each term
- [x] program counts total number of occurrences for a specified term
- [x] program calculates correlation of terms with a sentiment
- [x] program calculates correlation of a specified term with a sentiment
- [x] program allows user to perform any action with a the training set at any time by letting them type their own commands
<br/>
<br/>
By 6/19:
- [x] from the moment the training file loads, the program maintains a current "selection" of terms from the training file that the user wants to consider, defaulting to all of them
- [x] program allows user to view this selection table at any time
- [x] program allows users to specifically select or deselect certain terms
- [x] program allows user to specify upper and/or lower <i>numer-of-occurrences</i> thresholds that will automatically deselect any terms not between those bounds
- [x] program allows user to update those thresholds at any given time
- [x] program allows user to view "deselection" table at any time, which includes a reason for deselection
- [x] program allows user to "focus on" (meaning: view the state of) a specified term at any given time
- [x] program includes the following information in all of these tables: Term, Polarity, Count (# occurrences), Correlation with each sentiment, and Selection Status (and if deselected, how it was deselected. i.e. "deselected", "< threshold", or "> threshold")
- [x] user can sort any table they are about to print by any of its columns
<br/>
<br/>
By 6/22:
- [x] program asks user for a testing file and creates a "testingFile" object from it
- [x] program tests current model on the test file and prints the results
- [x] program saves the results locally to refer to in the next iteration of the program
- [x] program prints a visual representation of the test results as compared to previous tests
- [x] program allows user to type "help" at any time to learn about what they should do
- [x] program allows user to "explore" commands listed in the help menu to get further details about them
- [x] program handles improperly formatted/nonexistent training and testing files
- [x] program has an iterative interface
- [x] program allows user to exit (i.e. terminate) the program
<br/>
<br/>
Stretch Goals:
- [x] program gives a solid introduction to itself when it starts running
- [ ] program allows user to set polarity thresholds in addition to count thresholds
- [ ] program keeps track of the most accurate model you have built so far
- [ ] program allows you to revert back to the most accurate model you have built so far
- [ ] program allows the user to visualize a column of the last table they printed
- [ ] program allows user to save model in a comma separated format
- [ ] program allows user to open saved models
- [ ] program allows user to alter saved models
- [ ] program allows user to test with saved models
