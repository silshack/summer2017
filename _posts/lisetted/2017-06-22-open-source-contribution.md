---
layout: post
author: lisetted
title: "Lisette's Open Source contribution"
---


I am working on a project that involves data from the SEER cancer registry using a tool called SEER*stat. SEER*stat allows the user to use a point and click interface to query the SEER data for things like frequencies and rates. Since I know that I'll be pulling data from and modifiying the query regularly, I need to use a better querying tool to pull from SEER*stat so I can store my queries and also map colorectal cancer incidence across states. The tool at my disposal is R, and I found code by a guy named Anthony Damico who publishes his R code online in a github repository (https://github.com/ajdamico/asdfree/tree/master/Surveillance%20Epidemiology%20and%20End%20Results) to do what I need to do.

While running the code I had some errors, and it took me a couple minutes of trouble shooting to realize that the file name he had used in his code was for data up to 2013, but the data currently available is up to 2014 and the filename for the data has changed. I forked his code, and submitted a pull request noting the line of code to change (see link below). 

https://github.com/ajdamico/asdfree/pull/256

This was a relatively simple change, but did take some effort on my part since the error presented in my R session was actually in a later program file. The original author responded to my pull request within an hour to say thanks and also suggest I use a different R package to work with the SEER data.

This was a very rewarding experience. First it felt good to find the error while I was running the code since I am a bit of a rookie with R. It was gratifying for the original author to write back and acknowledge my contribution and merge it back into his code. And now I also know about another package that might be useful for my project. If this hadn't been an option for extra credit (even though this is past the due date and I wasn't sure if it would count), I would not have made the pull request. But now that I have done one request to fix code, I am very likely to do it in the future because I recognize the value in open source code and that I don't need to be afraid or embarassed to contribute to others' code. This has also made me think about what code of mine I should commit through github. I already use a commit function through SAS on my local files, but it might be useful to push it to github to help others. I also didn't think too much about how github can be a resource for my non-python and non-class needs.

Thanks for forcing me (kinda) into making this contribution!
