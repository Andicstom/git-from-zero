# git-from-zero
This is a step-by-step guide for learning most frequently occurring cases with git in a developer life.
## Introduction
When I started to use git it was hard to find well-tried practices. During the years I learned how to use the main and basic functionalities effectively. Of course there can be better or more simply solutions for some cases. Now I'd like to share my knowledge.
## Install git
First you have to install git which is really simple, no matter which OS you are using. You can find proper instructions on the official website:
https://git-scm.com/book/en/v2/Getting-Started-Installing-Git
## Basic terms
Let's talk about some terms related to version control and git! TODO
## 1. Fork and clone the repo | git clone [url]
Our dummy project consists of the chapters of Alice's adventures in Wonderland. Let's fork this repo with the button at the upper right hand corner! After that you have a copy where you can work. If you want to check it, just navigate to your GitHub profile and you can find it under the "Repositories" tab.

You can now clone your own copied repo to your dev machine by using this command in your proper local folder:

```git clone https://github.com/YOUR_GITHUB_USERNAME/git-from-zero.git```

This will actually make a local copy of your remote repo.
## 2. Check status | git status
At this point you are on the **master** branch which you can simply check like this:

```git status```

It also tells you how your stage look like and what kind of uncommited changes you have.

Since here everything is local, each branch should have a representation in the remote repository. These branch-pairs can have different names (I don't recommend it) but the remote one is marked with *origin*. So your local **master** branch is now up-to-date with the remote one: **origin/master**.
## 3. Create your first branch | git checkout -b [new-branch-name]
Since you work together with others on the same project, it's recommended to use separate branches for your tasks. Here you can do whatever you just want, it won't affect others. If you finished with your task, you can just simply merge your branch into the main one. What you should keep in mind: keep your main branch always consistent! It shouldn't contain half finished solutions.

So we are now on the **master** which is the main branch of our project. Let's say we noticed a bug and have to change the title of chapter 2. First, create your own brach:

```git checkout -b my-first-branch```

You can do your work now, change the title from "The Pool of T" to "The Pool of Tears"!
## 4. Stage and commit | git add [file_name] | git commit -m "[title]"
If you check the status now, you can see that *project/chapter_2.txt* was modified. First we have to add all of our changes to the stage otherwise they won't be commited:

```git add project/chapter_2.txt```

Note: If you have more than one modified files and you want to stage all of them, you can do it simply like this:

```git add .```

Let's check the status again! Git says "changes to be committed" so our modifications are ready for commit:

```git commit -m "Fix title bug" -m "Optional description comes here"```

The first "-m" option is mandatory and you can specify the title of commit with that. It is recommended not to use long titles: 50-60 characters should be enough! Title should explain WHAT does the given commit instead of HOW! For example "Fix XY crash" instead of "Check if XY object is null". The second "-m" is optional. If you want to add more detail what these changes do, you can specify it here.
## 5. Push
TODO
## 6. Create merge request
TODO
## 7. Pull and fetch
TODO
## 8. Amend and force push
TODO
## 9. Rebase
TODO
## 10. Interactive rebase
TODO
## 11. Stash
TODO
## 12. Go further
TODO
