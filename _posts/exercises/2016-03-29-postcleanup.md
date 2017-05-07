---
layout: post
author: elliott
categories:
  - exercise
title: "Clean up your posts from the year"
inclass: false
---

Alright!  You should have Cloud 9 and git set up.  You should be on a branch called `[yourname]-branch` mathcing your github user name. **Make sure you're not on gh-pages**.  If you are, revisit the `git checkout` step in the in-class exercise.

# Check the Site

View the class website that Cloud 9 is running for you at `[project-name]-[username].c9.io/spring2016/`.  If you don't see an application running, confirm that you have `spring2016/` with the trailing slash in your URL.  If you still don't see an application running, check on jekyll.  You'll need a terminal running this command to be active for your site to show up:

```
jekyll serve --watch --port=$PORT --host=$IP
```

# Fix the Site

Now, go to the People page and find you name.  Are all your posts showing up here?  If not, find them and check their YAML metadata.  Open a few recent posts in tabs.  Many of you had poorly formatted lists that were hard to spot on github (particularly Milestones posts).  Now with Jekyll you can add empty lines above and below your markdown lists and see the changes adter a few seconds.  

To fix a page, find the corresponding markdown in your folder, make changes, **save**, wait for Jekyll to do its thing, then reload the page.

# Commit your fixes.

**Triple check that you are not on the gh-pages branch**.  If so, revisit the instructions about about checking out a fresh branch for your user.  If you're on the branch you created abover you're in the right place.

Committing remotely is easy and fun.  It just takes a few more steps.

First, type `git status` to see what's up.

```
git status
```

You should see a bunch of the files you fixed in red.

Next, tell git what files you want to commit.  On github this was only one at a time but now we can do as many as we want.  We'll get more specific later but for now you can add them all.  The way we do that is with a `.` which means "here".  Git will find all changes in our current directory and its subdirectories for us.

```
git add .
```

Type `git status` to see what happened. **If you still have red stuff in your status** you may need to run `git add -A .`, which adds deleted and renamed files as well.  Case sensitive on the `-A`.

Now we can commit the changes that we've added.  Think of this as replacing the little commit message box on Github.  Think up a good commit message that describes what you've done.

```
git commit -m "Fixed [username]'s posts"
```

(If git complains about email addresses etc then you haven't finished setting up.  Revisit the set up how to on github.com)

The `-m` is for message and the string will be used as the commit message.

Now, to confirm that your commit is in the history, type

```
git log
```

This will bring up a list of all the commits, and yours should be on top.  **Press Q to exit**. 

Finally, type `git status` again to see what's up.

If you need to make more changes after you commit, go ahead!  Then repeat the steps above to add and commit your changes.

# Pushes & PRs

Once you've committed all your changes type `git status` to confirm there's nothing uncommitted.  Red stuff needs to be added and green stuff needs to be committed.

To push your commits to github, type

```
git push silshack [your-branch-name]
```

where `your-branch-name` is the exact name of the branch you made.

This pushed your code to github.com!  Now you can go to [https://github.com/silshack/spring2016](https://github.com/silshack/spring2016) and github should give you a convenient button to open a pull request right from there.  If not, create a new pull request with gh-pages as the *base* and your new branch as the comparison.

Whew!  Nice work.  You're a command line committer.

# Tips

* In Cloud 9's editor you can pick a gear icon and choose to Wrap Lines
* The Cloud 9 Run button is not going to be helpful to you
