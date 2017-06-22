---
layout: post
author: samsr31
title: "Sam's Final Project - Turtle Town!"
---

Here is my final project gamme: Turtle Town!


<iframe src="https://trinket.io/embed/python/5d414fb975" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>


Reflection:
The majority of this idea came to me pretty much fully formed.  I have had lots of extra ideas for extended features since then, but from the beginning, I wanted to make a town building game, with a set of different buildings that provide different resources, which you need to make more buildings.  The end goal of this game would be to upgrade your town center to a maximum level, representing a fully built town.
To get started on this, the first thing I knew I would need was a grid which players could click on to select a tile and build a building.  To do this, I set the screen coordinates to a specific size of pixels, created a grid square image which I could layer over the background, and did some math to compute the center and the boundaries of each grid square.  I then created an onclick function which used a for loop to compare each grid square in the dictionary to the click event coordinates, and which returned true if the click was inside the grid.  I then had the program record this square as the “selected” grid square, for use in other functions.
After getting the grid up and running, I hit a bit of a roadblock.  I had come up with some general milestones, and had a general idea of the features I wanted to add, but was not sure where to go next.  I also was uncertain what data I would need to track, and how to organize it all into dictionaries.  I had a lot of ideas of stats I probably should track, but no clear idea of how.  After thinking it over for a couple of days, and then talking with my group when we first met, I decided to get a system working to create “dummy” buildings which did nothing, and then use that as a template to add the other buildings.  Also, for game stats, I sat down and looked at them all as attributes of entities, like I learned to in Database 1, and organized them that way.  As I added the other buildings, I also started adding different resources, although they did not interact yet at this point.  The first resource that I fully implemented was money, so that you would have to pay something to build each building.  After I got that going, I got the program to start counting the other resources, even though they weren’t doing anything.  I then eventually added in checks to see if you had enough population to build a building, and enough power.  Lastly, I added a system for new townspeople to join your town, increasing its population, and had this system be limited by housing and fun.
While they work, these systems are not quite in a state which I am happy with.  Originally, I wanted to have population and power affect your town in a more subtle fashion.  Rather than acting as hard limits to how many buildings you could have, I wanted them to decide how many buildings counted as “on”.  You could spend money and buy a bunch of new houses, but if you ran into the negative on power, the game would have some of those houses go grey, and not add to your town’s stats.  Same with population: if you had more shops or power plants than you had workers, some of them would not operate, and not help your town until you drew in more people.  However, I had trouble thinking through how to implement this, and so the placeholder mechanic of requiring you to have enough power and population to open a new building remained.  Similarly, I wanted to make the population growth mechanic more dynamic than just “you get one new person per day, if you have room”.  As is, the placeholders I set up for that system to get it running are still in place.
After I got the basics of adding buildings done, I worked out how to delete buildings, and how to upgrade buildings to new levels.  I also started adding UI elements, to display information for the player.  I extended the screen size to add an info bar along the top, and worked out how to print text to that area.  One issue I hit on, which I have not yet solved, is how to write text over turtles.  Anything a turtle writes or draws is covered up by any other turtle in that area, regardless of the layering of those turtles.  So, for the top section of the screen, I had to leave a clear space where a turtle could write on the screen itself, with no turtles in the way.  For other UI elements, such as the help screen, I could not as easily remove turtles to get to the background, so I opted for writing out help messages in an image editor, and then displaying those images on turtles.  I also hit up against this problem with my game win animation.  I wanted to create little firework turtles which would shoot up out of the town center.  However, their lines get covered up by turtle buildings and the background grid turtle itself, so they are mostly obscured.  For now, this is one bug which I have not been able to fix.  I think I may be able to create a second screen object to layer over the first, and put these turtles on that upper screen, but I have not yet been able to try this in practice.
The last main thing I added to the game was a set of introductory screens, which the player must click through to get to the game.  These are followed by a difficulty selection screen, where the player selects easy, medium, or hard.  This determines how much each building can be upgraded, and therefore how long the game will take.  These were relatively easy to add in last, since the intro screens are just the help screens, but played before the game loop starts, and the difficulty settings just change a couple of variables in the building stat dictionary, limiting how much of the dictionary can be accessed.
Looking back on this project, one thing I would like to do better is planning out my milestones.  At the start, I wrote out all of the features I wanted to add, and felt like that was pretty good.  However, there were a few points where I got stuck, as the next milestone in my plan seemed too big to handle at once.  I’m not sure if I could have actually written out each itemized task I would need to do from the start, but whenever I hit one of these roadblocks, I found myself needing to step back, and try to break down the insurmountable milestone into parts.  As I went, I got in a better habit of occasionally stopping, looking ahead at my original feature milestones, and breaking a couple of them down into a plan of action for the day.
Also, interestingly, I found myself preferring to write out messy, repetitive code at first for some tasks, even if I knew I would probably come back and streamline it later.  I removed most of the examples of this, but left in one in my dictionaries.py module.  When I first plotted out the grid squares for the game, I literally wrote out a 64 item dictionary of dictionaries, with coordinates and boundaries for each grid square.  As I was doing this, I had a sense that this was probably something that I could do with a much smaller function, but it helped me to see everything that I was working with laid out to begin with.  This way, if anything didn’t work with the grid square selection, I could go look for a problem, rather than wonder if there was a problem in an algorithmically generated dictionary behind the scenes.  Then, later, once I was sure the system was working as intended, I went back and worked out how to pack the whole dictionary into a couple of for loops and some simple calculations.  This happened a few other times in my functions code, where I wrote out the same process multiple times, and then came back later and condensed or simplified everything.
Going forward, there are a bunch of extra things I would love to add to this game.  A save game feature is pretty high on my list, as well as a fire station building and a random chance for buildings to catch on fire and be destroyed.  Also, a tutorial for the game systems, a display for the actual costs of each building and upgrade, and more varied building graphics would help the game to communicate what was going on with a new player.
 
Here is my final milestone list.  As can be seen at the very end, I did not always work exactly in order, but jumped around to whatever next milestone seemed the most important / doable at the time.
 
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
- [x] Give that turtle a building type
- [x] Pull stats and an image from a dictionary of buildings
- [x] Cursor turtle which highlights selected square, deselects upon second click
- [x] Add the rest of the buildings, allow the player infinite money to build whatever for testing
- [x] Create a game loop clock, to periodically update game stats
- [x] Start with shops, make money, build more shops
- [x] Add building type to the grid dictionary
- [x] Have adding a building update the grid dictionary building type
- [x] Add the gameplay rules functions one by one, to check the various parts of the game state to see what you can or cannot build
- [x] Allow players to demolish a building
- [x] Have the demolish function also remove the building’s stats from the game state
- [x] Allow players to upgrade a building
- [x] Have upgrading a building change the game state stats
- [x] Fill out help screens, to inform the player of how to play, what does what
- [x] Add a small bar along the top which prints current resource values
- [x] Elaborate on TopNav
- [x] Add screen prompts to say why you can’t build or upgrade something, and when you win
- [x] Add a game win state when the town center is fully upgraded
- [x] Quality check - give the whole thing a pass to make sure everything is exhaustively explained / printed at each step, things are at least sort of balanced
- [x] Simple difficulty settings: harder modes have more building upgrades
- [x] Streamline code
- [ ] Fix fireworks win “bug”
- [x] Fix cursor size for town center
- [ ] Better population formulas
- [ ] Add saving, where the important game state variables are written to a txt file
- [x] Welcome screen(s)
- [ ] Add random fires and the fire station, which blocks them
- [ ] Add pop up ui elements when a player clicks on a square
- [ ] Add multiple levels, with different city maps
- [ ] Improve graphics
- [ ] Add turtle townspeople who wander around
