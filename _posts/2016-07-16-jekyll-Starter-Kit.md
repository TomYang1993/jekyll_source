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
We install Homebrew because we could use it to get [Rbnev](https://github.com/rbenv/rbenv) and install ruby, which is a very convenient way.  


### Xcode Command-line tools #
> The Command Line Tools Package is a small self-contained package available for download separately from [Xcode](https://en.wikipedia.org/wiki/Xcode) and that allows you to do command line development in OS X. It consists of two components: OS X SDK and command-line tools such as Clang, which are installed in /usr/bin.

![](https://developer.apple.com/library/ios/technotes/tn2339/Art/TN2339_InstallTools.png)

### Rubygem #
> Rubygem comes with the Ruby, but you may have to update to make sure your gem system is good  to go. Since jekyll is a ruby gem, if you want to use `gem` command to get it running, you must keep the system up to date. In the terminal, you can type in `gem update --system` to update. You can go to  <http://guides.rubygems.org/rubygems-basics/>  for more info.

### Rbnev or other ruby version control system#
> Use rbenv to pick a Ruby version for your application and guarantee that your development environment matches production. When you are doing a project, you can use newer version of ruby and also switch to older version when necessary, such as encountering some compatibility issues and so on.
