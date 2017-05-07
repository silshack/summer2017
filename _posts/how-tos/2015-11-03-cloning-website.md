---
layout: post
author: elliott
categories: how-to
title: Cloning and running our class website
published: false
---

You should already have created your development environment.  Using a command line terminal,

1. [Set up git](https://help.github.com/articles/set-up-git/)
2. [Generate your SSH keys](https://help.github.com/articles/generating-ssh-keys/)
3. `gem install github-pages`
4. `git clone git@github.com:silshack/spring2016.git`
5. `cd spring2016`
6. `jekyll serve --watch --port $PORT`

You should then see the site deployed at `https://silshack-eah13.c9.io/spring2016/`.  Note that the `spring2016/` *including the slash* is needed or your server won't be able to find the site's files