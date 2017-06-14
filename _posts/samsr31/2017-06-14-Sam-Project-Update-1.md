---
layout: post
author: samsr31
title: "Sam's Project Update 1"
---

Here is a current snapshot of my game:

<iframe src="https://trinket.io/embed/python/b7b98dabc7" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>


Reflection and Milestones:

Update - There is nothing to report, because no progress has been made.  Between our other assignments for today, and poor time management, and laptop failures, I haven’t been able to even look at my project for more than 30 minutes or so since yesterday’s class.  The one thing I did try to add is a while loop to keep track of the game’s state, and an in game clock.  I got that to work, but then it made other parts of my program break for reasons I don’t yet understand.  I tried to comment out different parts of what I did, and it seems like something to do with the while loop itself is causing other modules to not recognize variables from main.py, where the while loop is?  I would like to figure this out, and then get back to creating a simplified version of adding buildings to the screen.
 
Here is my milestone plan as it currently stands:
 
- [x] Make a grid layout for the town
- [x] Decide on building types
- [x] Town center, housing district, shops district, power plant, entertainment district, fire station
- [x] The Game Design: Buildings cost money to build.  They then need power and / or population to work.  Houses provide room for more population, but entertainment is needed to draw people to town.  Shops provide income, power plants provide power.  People randomly move to town if it has positive entertainment, or move away if it has negative.  Town Center provides some basic resources, so you can never go to zero.  Optional fire station defends against optional fires which might randomly burn down buildings.
- [ ] Create a dictionary with building stats to pull from
- [ ] Start with an empty dictionary
- [ ] Define the town center
- [ ] Define a dummy building
- [ ] Later, define additional buildings
- [ ] Create a separate dictionary for current game state values
- [ ] Make a dictionary with all relevant stats to be tracked or counted
- [ ] Start all values as zero
- [ ] Print values
- [ ] Create a dummy building to start, to test out clicking into squares and building something
- [ ] Create a new turtle
- [ ] Associate that turtle with a coordinate
- [ ] Give that turtle a building type
- [ ] Pull stats and an image from a dictionary of buildings
- [x] Cursor turtle which highlights selected square, deselects upon second click
- [ ] Add the rest of the buildings, allow the player infinite money to build whatever for testing
- [ ] Start with shops, make money, build more shops
- [ ] Add the gameplay rules functions one by one, to check the various parts of the game state to see what you can or cannot build
- [ ] Allow players to demolish a building
- [ ] Allow players to upgrade a building
- [ ] Fill out help screens, to inform the player of how to play, what does what
- [ ] Add a small bar along the top which prints current resource values
- [ ] Add a game win state when the town center is fully upgraded
- [ ] Quality check - give the whole thing a pass to make sure everything is exhaustively explained / printed at each step, things are at least sort of balanced
- [ ] Add saving, where the important game state variables are written to a txt file
- [ ] Add random fires and the fire station, which blocks them
- [ ] Add pop up ui elements when a player clicks on a square
- [ ] Add multiple levels, with different city maps
- [ ] Improve graphics
- [ ] Add turtle townspeople who wander around
 
