---
layout: post
author: alexreher
title: "alexreher's drawing app"
---

The app:
<iframe src="https://trinket.io/embed/python/cea637f2b5" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

### Initial Milestones

- [x] Drawing function
- [x] Brush Select
- [x] Color change
- [x] UI_toggle
- [ ] UI active color or brush
- [ ] Shape drawing
- [ ] RGB background
- [ ] Eraser

Reflection:
It was easy to come up with ideas for what I wanted, and I didn't have many milestones. Once I got to work on it though, I had some components that I should have broken down into smaller objectives. This probably would have helped me with controlling the scope of my initial milestones and making my approach to the coding easier.
I tended to try and get whole milestones done at once and then troubleshoot the succession of errors that would inevitably arise. At one point I was unable to get my UI to toggle as I wanted it to, it simply appeared when the probram ran. I spent hours stuck at this point, and ended up being blocked by the challenge of using variables across modules and some accidental  argument passing attempt from a keypress action. This was a really frustrating barrier to me, and derailed my plans for more features.

It was particularly annoying because I think some of the issues would have been spotted immediately if I'd approached it smaller iterations. I found this to work well days ago and identified the effectiveness of the strategy, but then on this I didn't put it into practice from the start. Once I restarted work on it with incremental steps, I ended up seeing the problem very quickly. Luckily, while I didn't feel like I had much time for breaks, I did skip around on milestones when I found myself stuck. This reduced the amount of time wasted. Still, with a pair programmer or another set of eyes, I think it would have been less of an issue to begin with.

Some planning would have also helped with the structure of my app. I divided it into three sections, but only after I'd made some progress on components that would end up across all the modules. While there's some organization, I think I may have split the file up a little more and also worked to reduce the need to send variables across modules or between the local and global scope. If I were to revise this, I think we could have done better with it. My understanding of how these worked grew as I was working, and I ended up eventually prioritizing function ahead of design due to time restraints.
### Final Milestones
- [x] Drawing function
- [x] Erase all function
- [x] Brush change function
- [x] Draw UI
- [x] Split file into modules
- [x] Draw Color Swatch
- [x] Make UI toggle 
- [x] Make Color Swatch clickable
- [x] Add keypress for colors
- [ ] Add RGB turtles
- [ ] Change background
- [ ] Eraser using background color
- [ ] Shapes
