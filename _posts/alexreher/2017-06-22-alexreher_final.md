---
layout: post
author: alexreher
title: "alexreher final project"
---

Embedded file
<iframe src="https://trinket.io/embed/python3/0134f46cae" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>


###Final Milestones
 - [x] Get data sample for textbooks
 - [x] File ingest
 - [x] Parse Call number ranges
 - [x] Make callnum dictionary
 - [x] Make the menu
 - [x] Add other file ingest options
 - [x] Instantiate classes for shelves
 - [x] Build visual for the shelf
 - [x] Add range/collection counts
 - [x] Add help function 
 - [x] Add LoC dict to help function
 - [x] Display shelves based on input
 - [x] Variable shelf options
 - [x] Range as percent of whole
 - [x] branch selection
 - [x] Update menu to reflect full range of options
 - [ ] Have Shelf density reflected visually
 - [ ] Display active collection/range selection on menu
 - [ ] Library comparisons
 
 
 
 Reflection
 
Concept
This project started off poorly. My initial vision and milestones were for an inter-library loan(ILL) visualization tool that would display the different locations around the world that we borrowed from (or loaned to, time permitting). I'd thought of being able to view the cities or schools in NC, each state, and countries outside the states. I waited as long as I could for data but eventually decided to start work with another set of data. This was not entirely bad. I now have access to the data I originally wanted, and it is incomplete and inconsistent. It'd make a challenge beyond my time and ability at this point.
I had to start working, so I grabbed some textbook lists from my work. A small part of my job is helping to manage the Textbook Collection at NCSU's Libraries. We have a copy of almost every required textbook that students need, with few exceptions. It's a big collection, split across two libraries. I thought I could look at these book lists and divide them up, show where we have more books at each library. I was still thinking of my old project idea, and thought of generalization that would let me reuse my code for the ILL idea, in time for the project, or just at a later date. 
As I worked I found the summing and min/max to be less interesting and started envisioning a shelving calculator that determines how much shelving is needed for a collection. I thought it would be something less conventional, and perhaps with some tenuous link to utility as my department wants to redesign its workspace. For flourishes, I could make the shelves look better, modify them by how densely packed they are, and if by some unlikely miracle I could manage it, have the density represented visually as well. As I worked in this new direction, my milestones shifted to reflect the new concept. They also gradually expanded as I went from thinking about the overall program to the actual implementation. After the drawing app I realized I was trying to do way too much at once, and making milestones that were bigger goals. These goals that combined several distinct actions into one step really didn't work with the more ambitious projects.
Process
Once I had some data, the first thing I did was import it. I knew that I was going to have several different function groups, so I immediately put it in a module of its own. I created a dictionary of call numbers and counts from this data. It was a holdover from some ideas related to my ILL project, and a desire to use dictionaries per the assignment requirements. Ultimately, as I learned more about dictionaries, it didn’t end up seeming like something I wanted so I commented it out. Usually I delete this type of stuff entirely, but I kept it for later reference.
As I worked on the call number range selection functions I knew I wanted to create another table that could get referenced by a number of future functions. I set up some global variables and pushed some of the menu out to another module. To take a break from trouble with getting the table reader to work as I wanted,  I shifted and built up the menu to contain the basic structure of my program. It gave me a sense of progress and a break from a source of mild frustration and stopped the ebbing of my confidence.
At this point I finally had a good grasp on what my class should be. This was one of those background thought problems that lasted for a while. I think others probably shared some of my tentativeness about classes, and I was reluctant to commit to something that might not work out or structurally not feel like an appropriate use. After reading about classes repeatedly and viewing examples(again, often the same ones repeatedly) it clicked. I felt like it wrote itself once the structure was figured out in my mind. Reality sunk in when I tried to run it though. It didn’t work. Again to avoid the shattering feelings of failure that I didn’t have the time for, I figured something else out.
I couldn’t really step away, we’re on tight deadline, so instead I changed direction to add a bunch of error checking to my menu and other inputs. I tidied up my range selection and when that was all done I saw a tiny typo in my class. At that point I had a class that could do some basic math and print a single shelf. I found a unicode book icon that I wanted to use, but held off on implementation. 
All my reading and re-reading of materials finally paid dividends when it came time to add a dictionary to my help function. I copied a list from wikipedia and then parsed it in Python. Thinking of future expansion to the project, I made the dictionary read headings and subheadings together. I thought the dictionary would eventually be the groundwork for a subject search helper function. The data is there, it just needs a bit of looping/character matching to let the user deep dive, either from the call number ranges or from the values associated with the keys. So a user could search american history and see that it’s in HA for example.
Finally I went in and generated some numerical comparisons and had the program output the appropriate number of shelves and then shelves based on density of books per shelf. 
While I’m happy with how lots of the code is organized and built, the coolness of the presentation never got to where I was happy with it. There was always another layer of complexity that I wanted to add. It would have been so much more satisfying to have the density of the shelving visually represented, or the shelves themselves look better. Time is always the enemy though. I’m glad that I spent the time where I did though. I feel like I crafted something that, while lacking in cool, was designed with thought behind it. I got to bring together a lot of what I learned without shoehorning anything in. I think my dictionary and class represented good uses of their respective forms.
Lessons
When I didn’t initially have the data I wanted, I didn’t panic, and I didn’t waste time. While transitioning from the old project idea to the new, I benefited from that mental work that occurs away from the keyboard. Some of my progress came out of the blue, and some from actively working through things in my mind, but it helped be be calm and focused when it came time to actually start coding. While the summer class has never given us as much flexibility with time to step back, it is unquestionably one of the key sort of coding philosophy takeaways that has an enormous impact on productivity and the feelings I have towards coding and problem solving.
When I began coding, the change in direction actually may have helped. I really liked trying to make functions and modules that were flexible enough for reuse based on different needs. Earlier on this would not have been my first instinct, I would have just tried to make the code work. I try to do the organizing and adaptable design from the beginning now. It helps conceptually, to have each module contain a collection of thematically related functions, and for each function to not get too bloated with what it does. I’ve found that when I build this way it leads me to want to try more experimentation. If I’ve created nice tools it’s not too hard to make something different with them. The downside to this is that I could just come up with ideas all day for stuff to add, let a project get unwieldy, and then run out of time to actually implement things. 
Sometimes the feature creep is an obstacle that I have trouble with. Because now I’m always trying to think ahead, I’ll occasionally start tackling the complex task of the ideal state rather than build my basic functionality, set it aside and then continue. That message was definitely imparted in class, but it hasn’t found its way into practice as much as I’d like. 
 
That said, I’ve been doing much more incremental progress. With many of my milestones there are several unwritten smaller tasks that I implement and test before marking the checkbox on my to-do list. I end up using print statements often, to check that values are being generated, modified or passed properly. While I’m still somewhat prone to the occasional syntax or close-but-not-quite logic error, this change to my work style has led to less frustration with problems and less time devoted to them. There’s rarely a large block of time that’s completely wasted by some overwhelming problem and the despair at not knowing where to begin in fixing it. Sometimes I will get ahead of myself (feature creep being the usual culprit) and then find myself in that position, far in advance of certain functionality. Now I know the way back though, and can usually find the problematic lines very quickly.
 
Solving problems has gotten easier as I find issues much quicker than I would when I just tried to code everything at once and then attempt to run it. Usually tracing my progress is enough for me to find the problem, and if I don’t get it right away I can test a few reasonable alternatives. At that point I’ll google the python documentation and usually get the answer there. Sometimes my old code, Stackoverflow or some other Python education site has the answers too. Those searches have gotten pretty quick. Part of it is practice, and the other part is probably having much more confidence in the jargon and my ability to read code. Earlier I might have stared at some snippet for a while, determined to make it fit my problem. I spend less time on that. Now a quick skim is often enough to get the gist of it, even if it’s using things I haven’t had first-hand experience with. I hadn’t used the operator module for instance, but reading about it, I felt like I understood it well enough.

 
 
