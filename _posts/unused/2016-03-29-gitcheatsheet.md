---
layout: post
title: "git cheatsheet"
category: how-to
published: false
---

# git clone

You can git clone a repo from github like this:

```
git clone https://github.com/silshack/spring2016.git
```

Get the url from the repo, and choose 'HTTPS'

# git branch & git checkout

You don't want to be working on the `gh-pages` or `master` branches.  Instead, create a new branch:

```
git checkout -b [branchname]
```

This says "create a new branch (from *here*) with name [branchname]".  *here* should be `gh-pages` (or master) and you'll
only need to do this once.  The `-b` is what tells git to make a new branch.  If the branch already exists and you
just want to go there, `git checkout [branchname]` will do that.

To see what branches you have, use

```
git branch
```

This will list them and put a little asterix next to the one you're on.

# git remote

A 'remote' is the url of a git repository on the Web.  You can type `git remote -v` to see
what remotes git knows about.  There's probably only one, the one it cloned from.

You can rename remotes.

```
git remote rename origin silshack
```

This renames our default-named origin branch 'silshack' for clarity.  Whenever you need to specify
a remote, for pushing or pulling for instance, use your remote's name.

# git status

Status is one of the most important commands.  Run it all the time!  It will tell you what your changes are (in red), 
if there are things that have been added but noe committed (in green) or if you're all committed up.

# git add

Adding files will make sure they're included in the next commit. You can add specific files like this:

```
git add path/to/mypost.md
```

where `path/to/mypost.md` should be replaced with the actual path to the file you want to commit.

Adding a file actually only adds the changes you've made to it after the last commit, if any.

You can also add ALL changes with

```
git add .
```

This means 'add all files *here*, including subdirectories.' To add all files in the repo, *here*
should mean the root of the repo. Use the unix commands `pwd` to print working directory and `cd [directory name]`
and `cd ..` to go into a directory and up out of a directory, respectively, if you're in the wrong place.

By default `git add` doesn't track file renames or deletions. You can tell this has happened if `git status`
shows some red `deleted:` files at the bottom after you're done committing.  To do that you'll need the `-A` flag:

```
git add -A .
```

## git commit

Once you've added some changes, you're ready to commit.

```
git commit -m "Your commit message here"
```

If you forget the `-m` you'll be taken into a text editor to exit your commit message.  Don't panic!  Edit and
save it if you can, or press `Ctrl-c` to exit the program if not.  Then `git status` to see where you are in the
process and pick up where you left off.

# git log

To see a list of commits, use 

```
git log
```

This will bring up a list of commits with the Unix program `less`.  If you haven't used `less`, here're the basics:
you can press space to page down, scroll with the arrow keys, and press `q` to quit.

In the list, you'll see a bunch of commit messages, commit ids.  Aren't you glad you've 
been making helpful commit messages?

# git push

Git push sends the commits from a branch you're on to a branch in a remote.  It's easiest to push from the branch
you're on to an identically titled branch on the remote. Since you're *never* committing directly to `gh-pages`, when
you do this you'll use your custom-named branch.  Also the below assumes your remote is titled 'silshack'.

```
git push silshack [branchname]
```

If you've made commits to the branch by other means (github.com maybe), you may get an error telling you you need to pull first.
If so, `git pull silshack [branchname]`.

# git pull

Sometimes you need to get commits from the remote, such as your classmates' posts or updated assignments.

```
git pull silshack gh-pages
```

You can replace `gh-pages` with another branch if you want something specific but since all the PRs get 
merged into gh-pages, this pull will get your current branch updated.

# git reset

Sometimes you need to un-commit things.  To do this, you'll need to use `git log` to get the commit id (that nasty long number) of the 
*last good commit*, and then reset back to that commit. Tip: you only need the first few numbers of the commit id.  This keep all the previously committed changes - 
you'll just need to add and recommit them.

```
git reset [commit id]
```

Warning: if you un-commit others' commits you will likely create conflicts that need to be resolved.

