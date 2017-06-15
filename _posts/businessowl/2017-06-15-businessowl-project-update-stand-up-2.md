---
layout: post
author: businessowl
title: "Aaron Plocharczyk's project update 1 post"
---
<strong>Here's the current trinket:</strong>
<iframe src="https://trinket.io/embed/python/eac50d79b3" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>
<br/>
<br/>
<strong>Progress since last class:</strong>
<br/>
Again, I worked on this project constantly because I have to fly to and be in a wedding this weekend. I am on track and working ahead to make time for that and other responsibilities that I have. I have now organized a lot of my code in a way that I thought made more sense. I now have 6 class files: Model, Selection, TrainingFile, TestingFile, File, and Reviews. Files are made up of reviews. TrainingFile and TestingFile extend File. Selection is associated with a specific TrainingFile and keeps track of what terms the user has selected as being necessary from the TrainingFile, as well as all the mathematical analysis of the terms. Model is build by a selection and can be used to test a TestingFile. In addition nto classes, I have two other modules, printer and interpreter. I believe printer is the same since last class. It prints lines and tables in a well formatted way. Interpreter, which takes all the commands from the user and executes them programmatically, has changed though. All the updates to the commands that interpreter accepts are specified in detail if you type "help" in the program after you specify your training file. But for now I'll just give you a sense of what I did with the commands I chose to accept. I really wanted to keep the experience of making a machine learning model as simple as possible for the user, so I came up with the idea of "selection" and "deselection" tables to abstract the notion of a machine learning model. So now the interpreter basically just accepts commands that all work based on the idea of a selection table. It lets the user set upper and lower number-of-occurrences bounds, deselect specific terms, select specific terms that had been deselected before, view whatever information they need, and test on a testing file path. It takes the user through the whole process without complicating it. Models and stats are built automatically, in the background, and the user doesn't have to do any of it. My program has gotten a lot cleaner, and I like it a lot. It's currently a working tool that allows you to build, test, and improve your machine learning models very easily. For next class, I will print out a visual representation of how accurate your current model is as compared to previous test that you've run.
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
- [ ] program prints and visualizes correlation and total number of occurrences for each term
- [x] program allows user to set a minimum threshold for total number of occurrences for each term
- [x] program allows user to delete particular terms
- [x] program allows user to restore particular terms that have been deleted
<br/>
<br/>
By 6/22:
- [ ] program asks user for a testing file and creates a "testingFile" object from it
- [ ] program tests current model on the test file and saves the results locally to refer to in the next iteration of the program
- [ ] program prints a visual representation of the test results as compared to previous tests
- [x] program allows user to type "help" at any time to learn about what they should do
- [x] program allows user to get further details about the commands listed in the help menu
- [ ] program repeats
<br/>
<br/>
Stretch Goals:
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
This is a stupidly amitious project for the amount of time I have, but I'm dedicating all the time I have to it, and it is working out well. I have spent 25-30+ hours on it so far and am certainly glad to be nearing the finish line because I'm running out of time to work on it. I am very happy with how it is turning out. I used it to build a prediction model and it is actually really useful and easy to use. I got my predictions to improve more than 5% in just a couple of minutes and the user experience is way better than I expected. It's a great little tool to have.
