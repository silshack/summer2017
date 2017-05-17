---
layout: post
author: elliott
categories:
  - exercise
title: "Clean up your posts for review"
inclass: false
published: false
---

Go through all of your posts from the year and fix anything that needs fixing.  Common errors I've seen:

- Your checkboxes don't work.  Make sure they are `- [ ]` or `- [x]`
- Your lists don't work.  Make sure they have empyt lines above and below
- Your in-line code blocks don't work.  Make sure your backticks match up.
- Your author or title fields in the YAML header are incorrect
- Your post(s) are not in the correct subdirectory.
- Your markdown headers, if you used them, don't render.  Make sure there's a space between your `#`s and the text and 
that the `#`s are at the beginning of a line.


# Updating your repo

Get ready to edit:

* `cd spring2016` if you're not already there.
* `git checkout` your existing branch if you're not already there.
* `jekyll serve --watch --host=$IP --port=$PORT` if it's not already running
* Open your running application in the URL you'll find in your Share menu.  Remember to add `/spring2016/` to the end of the url
* Update your branch with the latest from `gh-pages`: `git pull silshack gh-pages`.  If it tells you there's a conflict, that means git can'title: "Dictionaries are Wonderful"
* figure out which set of changes to keep.  Help it out by editing
the file to be the way it's supposed to be.  Git will have the version you pulled and the version you had in the file.  Delete 
and/or edit the lines to remove any `<<<<<<< HEAD` and `============` type stuff and make the text the way it needs to be. Afterwards
you can add and commit the conflict resolution like any other change.

While you can look at your posts straight from our github.io site, it'll be easier to do it with your own application.

You may have to do the above multiple times if you leave and come back to Cloud 9.  Use the information in your prompt to understand
the current state of where you are

# Edit a post

To edit a post, open it in Cloud 9, make changes and save.  Jekyll will then rebuild your site (which can take 20 seconds or so).
It will print `Regenerating: 1 file(s) changed at 2016-03-31 07:32:36`.  Once it also prints out `...done in 15.993689389 seconds.`, 
refresh the page to verify your changes did what you wanted.  Then repeat with the next post that needs help.

It may be useful to go thru your posts all at once in tabs, keeping the ones that need attention open for later.

If a partner post needs help, remember that it may be in their directory.

# Add, commit and push

Once you're done with one or more edits, use the instructions from last time and/or the [cheatsheet]({{site.baseurl}}/how-to/gitcheatsheet.md)
to push your changes up to github.

# Open a PR

Open a pull request with your newly created branch.

Take your time and find all the mistakes you can!  After this exercise is turned in, I will audit your posts looking for correct 
formatting.