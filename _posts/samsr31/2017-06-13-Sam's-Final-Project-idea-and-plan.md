---
layout: post
author: samsr31
title: "Sam's Final Project Idea and Plan"
---

Here I present for you… TurtleTown!


<iframe src="https://trinket.io/embed/python/5374b00102" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>


I love city/country/empire management sim games, such as Civilization, some older Sim games, and a bunch of Tycoon games from when I was younger, and this is a humble attempt to try out something small in that vein.  My basic concept is a game where you can click around in a grid, and then choose a building to make.  You spend money to build, and have to manage a few resources, like population, entertainment, money, and electrical power in order to build a bigger town.  In order to make it a game with “levels” which you can “win”, I’m thinking that there could be a central town square, which you can also level up as you go.  Building the town square up to max level wins the game!  Other buildings can also level up to give you more of their resource.
My current plan is to build a main “free play” mode, where players build a town, and try to upgrade it to the max.  If I have time, I could also design a few special maps with special rules, and string them together as a “campaign” of sorts.  In that vein, it may also be good to make a tutorial with a much smaller map, which even more explicitly explains what each thing does, and the general strategy.  Also, any extra time I have to work on this at the end will be spent on improving the graphics with pixel drawings from piskelapp.com .
 
Here are my milestones as they currently stand:
 
Make a grid layout for the town
Decide on building types
    Town center, housing district, shops district, power plant, entertainment district, fire station
    The Game Design: Buildings cost money to build.  They then need power and / or population to work.  Houses provide room for more population, but entertainment is needed to draw people to town.  Shops provide income, power plants provide power.  People randomly move to town if it has positive entertainment, or move away if it has negative.  Town Center provides some basic resources, so you can never go to zero.  Optional fire station defends against optional fires which might randomly burn down buildings.
Create a dictionary with building stats to pull from
Create a separate dictionary for current game state values
Create a dummy building to start, to test out clicking into squares and building something
    Cursor turtle which highlights selected square, deselects upon second click
Add the rest of the buildings, allow the player infinite money to build whatever for testing
Add the gameplay rules functions one by one, to check the various parts of the game state to see what you can or cannot build
Allow players to demolish a building
Allow players to upgrade a building
Fill out help screens, to inform the player of how to play, what does what
    Add a small bar along the top which prints current resource values
Add a game win state when the town center is fully upgraded
Quality check - give the whole thing a pass to make sure everything is exhaustively explained / printed at each step, things are at least sort of balanced
Add saving, where the important game state variables are written to a txt file
Add random fires and the fire station, which blocks them
Add pop up ui elements when a player clicks on a square
Add multiple levels, with different city maps
Improve graphics
Add turtle townspeople who wander around
    
