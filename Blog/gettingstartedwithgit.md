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
In this case, your comptuer is your home. 
All of your files would be your stuff and you have stuff in each room.

In this case, rooms are repositiories. 
Each room has stuff, each repository has files. 

Let's say you have really big rooms, so big that each room needs it's own moving truck. 
The moving truck is great, it travels at the speed of internet and is always there when you need it. 

How do you get your stuff in there to use the moving truck? 

There's a few steps to this. 

You take all of the stuff you want, and put it in a pile.

In git, this is done with `git add` the proper usage is:
```
git add <files to add>
```
This adds the files you specified to the pile.

In other words, adds the files to staging. 

But remember, you can only add files from the same room, or repository. 

Then you take the piles and box them up. You of course have to label the box. 

A `git commit` does this as well. 

Git commit takes all of the files from staging, and puts them a labeled box. The items are all in the exact same condition they were in when they were put in the box, the box will always be there in your house with the same label and condition captured, and they're also still accessible to you should you decide to keep using them. 

To make a commit:
```
git commit -m "Message about what you did"
```
Now that you have your stuff in a neat box, you will want to get it on the truck. 

Use `git push` to do this. 

It takes your commits and pushes them to your repository. 

In other words git push takes your boxes and pushes them on to the moving truck. 

To push:

```
git push
```

Now your commits are pushed to the git server. 

In other words, your neatly packed boxes of stuff have been put on the on the moving truck and are accessible from anywhere. 

You can verify this by visiting the website with the repo. 

 To do this, go to https://github.com and log in.
 
 Click on the repo and you should see your files with the changes you made. 

