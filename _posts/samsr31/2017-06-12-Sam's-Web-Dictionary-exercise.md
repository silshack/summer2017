---
layout: post
author: samsr31
title: "Sam's Web Dictionary exercise"
---

Here is my homework:

<iframe src="https://trinket.io/embed/python3/a5fa878a97" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

And here is my reflection:

This exercise seemed more helpful as an additional practice of how to pull from a dictionary than how to access web data.  The JSON sections of code mostly seem to make sense, but I will need to probably rewrite them a few times myself to get them down for sure.
As for the assignment itself, it was actually sort of hard to decide on four interesting bits of information to pull out.  Most of the information being pulled in from google seemed to focus on latitude/longitude and atomized address information.  I ended up focusing on the location’s ‘types’, which seemed fun and descriptive, as well as the ‘location_type’, which changed depending on how exact the address was.  That field was always one string of data, but I realized after my first attempt that the descriptive type list could be more than just two descriptors, like I originally thought.  So, I redid that part as a for loop, so that it could handle more or less than two type descriptors.
