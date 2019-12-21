---
tags: [Git Tutorial]
title: 4 The Basics
created: '2019-12-12T12:59:09.142Z'
modified: '2019-12-12T15:11:29.049Z'
---

# 4 The Basics

I think this covers the most important things to use Git in your daily life.

I think it is useful to use the comand line to get a grip on how everything is working, but later you can also use your favorite GUI.

## Three stages
A file in Git is always in one of these three stages:
* modified
* added
* committed

This is so you have heard of it, we will come back to that in a second.

## Creating a Git repository

You can create a Git repository from any directory on your computer, it doesn't matter if it's empty or you got already stuff in there. 

For now, create a new directory and change into it:

    $ mkdir my-repo
    $ cd my-repo

Now create a repo:

    $ git init

If you installed the git-prompt earlier, your comand line should look like this now:

    $ ~/temp/my-repo(master) >>

Use 
    
    $ git status

to see a bit of information about your newly created repository.

## A new file

As *git status* has already told you: There is nothing in your repository. So let's add something. Create a text file in the repository using the tool of your choice.

Having done that and running *git status* again tells you something like this.

    On branch master

    No commits yet

    Untracked files:
      (use "git add <file>..." to include in what will be committed)
      my_first_file.py

    nothing added to commit but untracked files present (use "git add" to track)

It is already giving you a hint on what to do next: Add the file to keep track of the file:

    $ git add my_first_file.py

Or, when you want to add everything in the directory:

    $ git add .

Running git status again says

    On branch master

    No commits yet

    Changes to be committed:
      (use "git rm --cached <file>..." to unstage)
      new file:   my_first_file.py

Next step: Commit your changes to the repositry:

    $ git commit

This is now opening a text editor (you maybe set that earlier, remember?) and prompts you for a commit message. Here you can say what the commit is about. There are a couple of best practice things about these message, for now just write whatever you like.

Running *git status* again now gives you the information that everything is clean on your repository now.

Now try *git log* and see what that tells you.

## Changes

Open your file again and change saomething. Run *git status* again. It tells you, that the file is now modified.

Running  

      $ git diff

gives you details about what you changed

You can now add your changes.

To add, just do as before:

    $ git add .
    $ git commit

When you run *git log* again you can now see that you added a new commit.

When running *git log* you can see something like *1d762e7be0265350750ed9fc3b17c346d8c19b0b* being shown. This is the key to this commit. It will never change, you can use this to reference a commit later to work with it.

## Resetting changes

Imagine you did some changes to your file but found out that this was not what you wanted. You can reset your changes. Do some changes to your file now and then run:

    $ git status
    $ git reset --hard HEAD
    $ git status

You can now see that all your changes are gone and the original file is back.
    
   

