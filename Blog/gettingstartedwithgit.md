# Getting Started With Git 

This is by no means a comprehensive guide to git. 
Rather it is geared to novice programmers in order to expose them to the idea of using git, as well as showing them how. 
 
### Why The Need For This?
 ---

 Often new programmers have not heard of git, nor thought of version control. 
 It is likely most will have heard of it, but not used it until working with a team on a project. 
 While Git may be a great tool for this, it can be rather unforgiving when mistakes are made. 
 <br> <br>
 But making mistakes is inevitable. 
 Git fine honed sword, but one slip of the hand and you will get cut. 
 Whether you accidently rebase instead of merging, or everyone on your team forks the repository instead of cloning it, mistakes will be made. 
 And you know what? 
 Thats okay. <br><br>
If you learn now, before you and your team is trying to learn how it works, you will be reducing the learning curve. 
With such a complex program, this is good. 

## TODO FINISH ME 
You will be able to 

### Downloading And Installing Git
---
### Making a Github Account And Why You Want One
---

### Git Is Like A Moving Truck
---

That's exactly how you should think of it. 
Like you are constantly moving. 
We'll assume that you are at home right now.
In this case, your computer is your home. 
All of your files would be your stuff and you have stuff in each room.

In this case, rooms are repositories. 
Each room has stuff, each repository has files. 

Let's say you have really big rooms, so big that each room needs it's own moving truck. 
The moving truck is great, it travels at the speed of internet and is always there when you need it. 

How do you get your stuff in there to use the moving truck? 

There are a few steps to this, and it's not as complicated as it might seem at first. 

### Git Add
---

You take all of the stuff you want, and put it in a pile.

In git, this is done with `git add` the proper usage is:
```properties
git add <files to add>
```
This adds the files you specified to the pile.

In other words, adds the files to staging. 

But remember, you can only add files from the same room, or repository. 

![Related Image](https://pics.me.me/thumb_hal-9000-im-sorry-dave-i-cant-do-that-com-14978728.png "Image Hover Title")


### Git Commit
--- 

Then you take the piles and box them up. You of course have to label the box. 

A `git commit` does this as well. 

Git commit takes all of the files from staging, and puts them a labeled box. The items are all in the exact same condition they were in when they were put in the box, the box will always be there in your house with the same label and condition captured, and they're also still accessible to you should you decide to keep using them. 

To make a commit:
```properties
git commit -m "Message about what you did"
```
![Related Image](https://pics.me.me/thumb_hal-9000-im-sorry-dave-i-cant-do-that-com-14978728.png "Image Hover Title")

### Git Push
---

Now that you have your stuff in a neat box, you will want to get it on the truck. 

Use `git push` to do this. 

It takes your commits and pushes them to your repository. 

In other words git push takes your boxes and pushes them on to the moving truck. 

To push:

```properties
git push
```

Now your commits are pushed to the git server. 

In other words, your neatly packed boxes of stuff have been put on the moving truck and are accessible from anywhere. 

You can verify this by visiting the website with the repo. 

To do this, go to [github.com](https://github.com) and log in.
 
Click on the repo and you should see your files with the changes you made. 


![Related Image](https://pics.me.me/thumb_hal-9000-im-sorry-dave-i-cant-do-that-com-14978728.png "Image Hover Title")

### Git Fetch
---

Now that your commits are pushed to your git server, you need to be able to get the files on any computer. 

First you need to check if there any updates. 

This is done with `git fetch`. 

Git fetch gets the new data from a repo. 

It's like taking the boxes from the moving truck to get your stuff. 

```properties
git fetch
```

Now that you know what has changed, you are able to to pull the stuff out and put it in the corresponding room in your new place. 

Before we move further, there is something about git that you should know. 

While the entire file is captured in each commit, it is worth noting that git actually works by tracking the changes made to the files. 

Git fetch is just getting changes that might not be on you local machine. 


![Related Image](https://pics.me.me/thumb_hal-9000-im-sorry-dave-i-cant-do-that-com-14978728.png "Image Hover Title")

### Git Pull
---

Now we need to update the files on our local machine with the updated versions that we just fetched. 

Essentially, we are unpacking the boxes that we just got from the moving truck. 

To do this, we use `git pull`. 

```properties
git pull
```

But how does this work given that git tracks the changes?

Think of it as instead of getting rid of your old stuff and replacing it each time, git tracks the changes made to the stuff, and updates it with the changes. 

So when you use git pull on a different device, instead of deleting the already present files, the changes from the repo are merged with your local files. 

The end result is the same, your files are are the same as what it is in the repo.

Think of it as going to the same room in another house, and it's exactly like what you had before. 
<br>
<br>
Under the hood, git pull actually does a git fetch and a git merge, but that is beyond the scope of this guide. 

It is a good habit to get into to fetch before you pull, in case there are changes that you forgot about.

This comes more into play once you start diving deeper into git. 

![Related Image](https://pics.me.me/thumb_hal-9000-im-sorry-dave-i-cant-do-that-com-14978728.png "Image Hover Title")

### Other Useful Knowledge
----

* IF you are in your main project folder, `git add .  `{:.properties} will add all of your files and directories, as well as any nested files or directories. 

* There are some files that you may not want to track with git as they can cause issues across multiple machines.
Adding a `.gitignore` file deals with this issue pretty well. 
To do this, make a new file in your repo called `.gitignore` and list the files and directories that you do not want tracked.
It can sometimes be a guessing game as which files you need to ignore and which you don't.
Luckily, [gitignore.io](https://gitignore.io) is a handy site to help you make your `.gitignore` files.  
  
  On the site, type in the programming language(s) and operating system(s) you are using and press create. <br>
  A new page will appear with an auto-generated list of files of extensions to be ignored.  <br> 
  Simply copy and paste this into your `.gitignore` and you should be off to a good start.  
  It may not always have everything you want to ignore, but it's very useful and removes a lot of the guesswork.  
  > Mac users should note that this is especially useful for them, as it is very common to see the `.DS_Store` file get pulled into repositories. It is not a file that you need and the generated values do account for this. 

* Commit (and push) every time you add a feature, fix some issues, make significant progress, or feel you need to save your work. 
This is a very good habit to get into.
Doing so makes it easier to identify a change that broke part of your program and revert to a time when it worked. 
Having many small commits, as opposed to one large one, is also extremely useful later on when you are working with a team. 
Not to mention that you will have more work saved in the cloud in case of an unfortunate event such as your computer dying or crashing. 

### Further Steps
---

A collection of resources about git: [try.github.io](https://try.github.io)

The official tutorial made by git: [git-scm.com/docs/gittutorial](https://git-scm.com/docs/gittutorial) 

A game to learn git: [learngitbranching.js.org](https://learngitbranching.js.org/)

### Recap
---
