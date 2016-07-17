---
layout: post
title:  "Jekyll starter kit!"
---
## Introduction #
This article is for a completely new beginner as a developer. It states how to start a jekyll post on a github host page. Senior developers or junior developers may be very familiar with these basics. As a beginner myself, I just make this article for interest and a record for my very first developer experience. I hope that after reading the article anyone can start doing something with their terminal, with their text editor and find interest in coding. Mistakes may be possible through the article. I hope anyone who find mistakes can reach me and I can learn from you guys.

----
----

## Head-ups #
Firstly, we must set up the environment for the whole process, just like preparing  
all the tools before we are going to build something.  

### Homebrew #
> Homebrew complements OS X and installs software you can not install with OS X. It will provide dependencies for your [gems](http://guides.rubygems.org/). (When you are using a fresh mac which has a clean software  
environment, system may ask you for Xcode Command-line tools when you are installing Homebrew.)
We install Homebrew because we could use it to get [Rbnev](https://github.com/rbenv/rbenv) and install ruby, which is a very convenient way to get ruby ready and manage Ruby versions.  


### Xcode Command-line tools #
> The Command Line Tools Package is a small self-contained package available for download separately from [Xcode](https://en.wikipedia.org/wiki/Xcode) and that allows you to do command line development in OS X. It consists of two components: OS X SDK and command-line tools such as Clang, which are installed in /usr/bin.

![](https://developer.apple.com/library/ios/technotes/tn2339/Art/TN2339_InstallTools.png)

### Rubygem #
> Rubygem comes with the Ruby, but you may have to update to make sure your gem system is good  to go. Since jekyll is a ruby gem, if you want to use `gem` command to get it running, you must keep the system up to date. In the terminal, you can type in `gem update --system` to update. You can go to  <http://guides.rubygems.org/rubygems-basics/>  for more info.

### Rbnev or other ruby version control system#
> Use rbenv to pick a Ruby version for your application and guarantee that your development environment matches production. When you are doing a project, you can use newer version of ruby and also switch to older version when necessary, such as encountering some compatibility issues and so on.  

-----------
------------

## Install jekyll #
You can go to the official website <https://jekyllrb.com/> for the quick-start instructions.  
Or you can follow the commands.  
`gem install jekyll` will install jekyll for you.  
`jekyll new the-name-of-my-site` "the name of my site " is up to you and this will be the directory name under your user directory.  
`cd the-name-of-my-site` will take you into the directory of your blog.
And if the commands above all work fine then you should have no problem show your default blog on your local server.  
`jekyll serve` will set up your blog on your local server.  
When you hit "enter", there will be a lot of messages shown below, find "server address:" and the default is 4000, so you can go to your browser and enter `http://localhost:4000`  
Lucky enough, you can see your page now!!!

---------
---------

## Host jekyll on your github #

So now you can see your own blog on the local server, how can you make it available for everyone on the internet? You just push it to the github!

#### Firstly, you must track all the changes in our directory and commit those changes in your local directory.  #

 1. Go to the terminal, `cd` to the root directory of your blog,which is maybe `~/the-name-of-my-site`,and `git init`. This will make all your files trackable.  
 2. Then you can make changes to all kinds of files in your directory, and git will compare and know what you have done. Once you want to make these changes valid, you can `git add --all`,then `git commit -m "the message you want to record about these changes "`. Now your changes are valid and files in the git have been changed to the latest version. Or you don't know what you should change for now, you can just `git add --all` and `git commit -m ""` for initialize your git because `git init` creates an empty git, you at least have to give it something.
 3. when you make sure your changes are ready, your page is good enough, you can push it to the host page, to the public.

#### Then you should create a host place for your blog on a web server, it's not local anymore.

  1. Go to your github account(make sure you have one!) and create a new repository.
  2. Name it as `directory name of your blog.github.io`.
  3. Now we are going to push it to an existing repository, which is the root directory of your blog which holds all your file about the blog. Go to terminal, `git remote add origin the-address-of-your-blog-which-is-identified-by-github` this will connect your local root directory to a github address so github knows where to find these origin files.
  4. `git push -u origin master` this is the final step and now you could see the website on a web server!
  5. In the browser, type in `https://your-repository-name.github.io` and you can see it live.

## To Be Continued #
Now you can see a empty page(not completely empty, should have some default appearances), so how can we post? Wait until my next post!
