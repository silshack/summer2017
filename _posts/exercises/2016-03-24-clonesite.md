---
layout: post
author: elliott
categories:
  - exercise
title: "Clone and run our class website"
inclass: true
---


Final git setup step:

```
git config --global core.editor "nano"
```

This keeps you from getting lost in vim.

```
git remote rename origin silshack
```

This renames our default-named origin branch 'silshack' for clarity.

# Clone

From Cloud 9:

```
git clone https://github.com/silshack/spring2016.git
```

(unless you set up SSH, in which case you should pick the SSH url from our class repo)

# Run

```
# Change into the new directory
cd spring2016

# Command line tip: start typing something and press tab to autocomplete
# sp<tab> will sutocomplete to spring2016.

# Install stuff
bundle install

# Make a new branch
git checkout -b [your-github-name]-branch 

# (e.g. mine would be git checkout -b eah13-branch 

# Start Jekyll (the port and host stuff is Cloud 9 specific)
jekyll serve --watch --port=$PORT --host=$IP
```

You'll then be able to see your version of our website at:

`[c9-project-name]-[username].c9.io/spring2016/`

Where c9-project-name is the name of your Cloud 9 workspace. Note the `spring2016/`! The trailing slash is important.

# Tips 

* You can press `Ctrl-C` in the Terminal to kill this process if you need to.  
* Press the up arrow to fill the command line with a previous command you typed
* You can open a second terminal in Cloud 9 with a + button. if you open a second termina, be sure to `cd spring2016` because it will start you out in the workspace folder.

For your next assignment, you'll be editing your .md files.  You should be able to see your changes show up a few seconds after your save.  Watch the terminal for an indication that things are done.