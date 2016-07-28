---
layout: post
title:  "Git and Github"
---
![](https://git-scm.com/images/logo@2x.png)

## What is Git ?? #
Linus Torvalds is the developer of Git, and he describes Git as "the stupid content tracker". So git is a tracker, it tracks the changes of files and projects and controls them. So technically speaking, git is a version control system that is used for software development and other version control tasks.

Linus Torvalds quipped about the name *git* (which means "unpleasant person" in British English slang): "I'm an egotistical bastard, and I name all my projects after myself. First 'Linux', now 'git'." He is a genius.

-------------------------  

Here's a workflow taken from the blog in git's official website which may help you understand.([Original blog is here!](https://git-scm.com/blog))

Let's visualize this process. Say you go into a new directory with a single file in it. We'll call this V1 of the file and we'll indicate it in blue. Now we run `git init`, which will create a Git repository with a HEAD reference that points to an unborn branch (aka, nothing)

![](https://git-scm.com/images/reset/ex2.png)

At this point, only the Working Directory tree has any content.

Now we want to commit this file, so we use `git add` to take content in your Working Directory and populate our Index with the updated content

![](https://git-scm.com/images/reset/ex2.png)

Then we run `git commit` to take what the Index looks like now and save it as a permanent snapshot pointed to by a commit, which HEAD is then updated to point at.

![](https://git-scm.com/images/reset/ex4.png)

At this point, all three of the trees are the same. If we run `git status` now, we'll see no changes because they're all the same.

Now we want to make a change to that file and commit it. We will go through the same process. First we change the file in our working directory.

![](https://git-scm.com/images/reset/ex5.png)

If we run `git status` right now we'll see the file in red as "changed but not updated" because that entry differs between our Index and our Working Directory. Next we run `git add` on it to stage it into our Index.

![](https://git-scm.com/images/reset/ex6.png)

At this point if we run git status we will see the file in green under 'Changes to be Committed' because the Index and HEAD differ - that is, our proposed next commit is now different from our last commit. Those are the entries we will see as 'to be Committed'. Finally, we run `git commit` to finalize the commit.

![](https://git-scm.com/images/reset/ex7.png)

Now `git status` will give us no output because all three trees are the same.

Switching branches or cloning goes through a similar process. When you checkout a branch, it changes HEAD to point to the new commit, populates your Index with the snapshot of that commit, then checks out the contents of the files in your Index into your Working Directory.

So now you should have a general understanding of Git, and Git has more commands and usage that you may not encounter. You should dig in more with wiki and [Git official website](https://git-scm.com/).

## What is Github ?? #
Github is more like a online version of Git, using the same core. However, github is more versatile and human-friendly. Github has a graphic user interface and is easier for freshman to understand and git has only the terminal interface( git now has GUI but is not powerful as github and developers prefer the terminal.)

Technically speaking, is a web-based Git repository hosting service. It offers all of the distributed revision control and source code management (SCM) functionality of Git as well as adding its own features.

You can follow the [tutorial](https://guides.github.com/activities/hello-world/) and understand the similarity between github and git.

## Control your project !! #
Git is for your local control and Github is for your online control. If you want to revise your project and push your project to a public repository, how could you do that? With git and github, you can do that!

Here's an example that explains briefly about how it works.
Check my "Terminal is your friend !" post for the terminal commands.

Firstly, we create a file inside our test directory.

![](/assets/Screen Shot 2016-07-28 at 1.12.00 PM.png)

Then, we `git init` in the directory, and we get an empty repository. `git add --all` will add these changes to the empty repository because we have a `test.rb` now. `git commit -m "first try"` will refresh git repository and change permanently.

![](/assets/Screen Shot 2016-07-28 at 1.13.00 PM.png)

Now we have taken care of the local part. Let's go online !

Firstly, we will create a new repository on the github page.

![](/assets/Screen Shot 2016-07-28 at 1.14.09 PM.png)

![](/assets/Screen Shot 2016-07-28 at 1.14.26 PM.png)

Then we get the page that set up the repository. `git remote add origin` means that Github will give you a path to connect your local directory or project to the online hosting service, then from now on your local directory will know where to find the online hosting service. `git push -u origin master` means you can push your local repository online !

![](/assets/Screen Shot 2016-07-28 at 1.14.38 PM.png)

![](/assets/Screen Shot 2016-07-28 at 1.16.59 PM.png)

Refresh ! And you can see your whole new repository !

![](/assets/Screen Shot 2016-07-28 at 1.17.16 PM.png)
