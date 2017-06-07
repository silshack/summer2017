---
layout: post
author: nvola
title: "Natasha's Poetry Slam Files Exercise"
---
I first started with the basic requirements of having the capability to save the user's poem to a file. Because my program has the user enter the poem line-by-line and the line is printed after the user enters it, I created an emtpy list at the top of the program. When the user indicates they are done with their poem, the user is prompted to name the file and a file is created with that name and the poem list is stored to that file line by line. I chose this method (of storing each line as an item in a list) because it worked well with the existing method where each line was printed.

<iframe src="https://trinket.io/embed/python/54cb93f171?start=result" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>



Having met those requirements, I decided to attempt allowing a user to enter a file which the program then reads and prints to the screen. The program now asks for the users input to get the name of the file to read. The code reads each line in the file, strips it of trailing spaces, cuts the length of each string to 35 characters (the number of characters I had originally chosen as a good amount to fit on the screen given the font and size), and stores each line to a poem list. The program then runs through the poem list and each line is written on the screen. The user is then prompted whether they want to input another file, and the screen is cleared. I didn't have time to try to merge the two requirements (hence the two trinkets embedded), so the lower one only allows a user to upload a file, not to enter poetry and save it to a file as in the previous program.

<iframe src="https://trinket.io/embed/python/e64709aa58?start=result" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>
