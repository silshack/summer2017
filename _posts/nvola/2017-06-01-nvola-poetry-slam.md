---
layout: post
author: nvola
title: "Natasha's Poetry Slam Exercise"
---

Here is my Poetry Slam Exercise: 

<iframe src="https://trinket.io/embed/python/eda6fcdf0c" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>



The first thing I tackled was coding the ```while``` loop to continue asking for user input for the various lines of poetry. With the previous exercises utilizing ```while``` loops this was very easy to do. I then requested additional user input so that the author could enter their name and that shows up on the bottom of the screen when they're done. Having satisfied the basic requirements, I decided to add a black border around the poetry to make the output text look a bit nicely formatted; this required some re-calibrating of coordinates I had previuosly entered in the main code, but wasn't too strenuous.



Then, I had a number of unsuccessful attempts (and almost gave up on) having the program split up really long lines of text (horizontal overflow). I spent a lot of time reading about list and string methods, and about fonts and font widths. Eventually, I decided to just test what length of string would be "too much" to fit within the border I'd created for my program; after additional testing I chose a more conservative list length (35) to hopefully accomodate for wider text caused by wider characters. After this, I decided another ```while``` loop was necessary given the uncertain length of the user's input each time; then it was just a matter of testing to make sure it was chopping the user input where it needed to be doing so.  



With additional time, not only would I have liked to work on the other additional requirement regarding too many lines of text (vertical overflow), but I'd also want to work on splitting up the long lines of text in legible/sensible ways. The current method just chops the lines at the specific length I'd chosen (35 characters), without regard for where in the line it's chopping; obviously, when we write we split up lines in places that make sense (e.g., at the spaces between words, or between syllables using a hypen to indicate that the rest of the word continues on the next line). 

