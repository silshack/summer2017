---
layout: post
author: businessowl
title: "Aaron Plocharczyk's project idea and work plan post"
---
<strong>Project Idea:</strong>
<br/>
I had a lot of trouble coming up with something to do for my final project. I actually started on an idea that I don't find very interesting. I was parsing the exceptions that php throws in errorlog files and was going to do analysis on that. I could not come up with anything better to do and had to get a head start to make up for the heavy workload of my job this week. I actually got relatively far but I'm not interested in the project, so I'd rather scrap it and put effort into something I care about and will work hard on than make something just to satisfy the requirements. Even now that I don't have the weekend to work and will have less time to work on it this coming week, I think it's the right move. Here's what I have made and am scrapping:
<iframe src="https://trinket.io/embed/python/74d189bab8" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>
I ultimately ended up on doing sentement analysis for reviews found online. Sentiment analysis is very useful in the real world because it can be used for machine learning. You can use what you learn from sentiment analysis programs like the one I plan to build to make a "model" that a machine can use to learn to make predictions on reviews in the future. <a href="https://archive.ics.uci.edu/ml/datasets/Sentiment+Labelled+Sentences" target="_blank">This awesome website</a> gives me a bunch of reviews that have been prelabeled as either having a positive or negative sentiment. It gives me three files: amazon, yelp, and imdb. Sentiment analysis is much more interesting to me and there are a lot of different things I can do with it.
<br/>
It will certainly be useful to have the program be able to analyze each file independently in terms of review length, word count, common words, etc. But it might also be interesting to see if I can make the files interact at all if I have time to do so.
<br/>
<strong>Work Plan:</strong>
- Upload data files
- Create main.py
- Create analysis_tools.py
- Create an iterative loop for the program to run in
- Allow user to type "Help" at any time to gain insight on what to do next
- Allow user to specify file name
- Allow user to access max/min/average <strong>review length</strong> for all types of sentiment reviews (or for a specific sentiment type) in the file
- Allow user to access max/min/average <strong>word count</strong> for all types of sentiment reviews (or for a specific sentiment type) in the file
- Allow user to access <strong>most common words</strong> in all types of sentiment reviews (or for a specific sentiment type) in the file
- Allow user to access <strong>least common words</strong> in all types of sentiment reviews (or for a specific sentiment type) in the file
- Allow user to access <strong>most correlated words</strong> to a specific sentiment type in the file
- Allow user to set a <strong>"threshold"</strong> for correlation so that a term must occur at least n times before it is considered
- Allow user to see <strong>correlation of word count/review length</strong> to a specific sentiment type in the file
- Allow user to view <strong>terms that are unique</strong> to a certain file
- Allow user to visualize results of these queries
