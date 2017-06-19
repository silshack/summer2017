---
layout: post
author: samsr31
title: "Sam's Third Project Update"
---


<iframe src="https://trinket.io/embed/python/3023e53c1d" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>


Update - The main thing I got done this weekend was to revise and improve the graphics images I plan to use for my game.  Before, all of the buildings were represented by hastily scrawled letters identifying what type of building they were.  Now, they are represented by little color-coded houses, with different numbers of houses for different levels of building.  Up next, I plan to figure out an ontimer function to update game state stats, and an always present menu bar to display current stats.
 
 
Here is my milestone plan as it currently stands:
 
- [x] Make a grid layout for the town
- [x] Decide on building types
- [x] Town center, housing district, shops district, power plant, entertainment district, fire station
- [x] The Game Design: Buildings cost money to build.  They then need power and / or population to work.  Houses provide room for more population, but entertainment is needed to draw people to town.  Shops provide income, power plants provide power.  People randomly move to town if it has positive entertainment, or move away if it has negative.  Town Center provides some basic resources, so you can never go to zero.  Optional fire station defends against optional fires which might randomly burn down buildings.
- [x] Create a dictionary with building stats to pull from
- [x] Start with an empty dictionary
- [x] Define the town center
- [x] Define a dummy building
- [x] Later, define additional buildings
- [x] Create a separate dictionary for current game state values
- [x] Make a dictionary with all relevant stats to be tracked or counted
- [x] Start all values as zero
- [x] Create a dummy building to start, to test out clicking into squares and building something
- [x] Create a new turtle
- [x] Associate that turtle with a coordinate
- [ ] Give that turtle a building type
- [x] Pull stats and an image from a dictionary of buildings
- [x] Cursor turtle which highlights selected square, deselects upon second click
- [x] Add the rest of the buildings, allow the player infinite money to build whatever for testing
- [ ] Create a game loop clock, to periodically update game stats
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
 
