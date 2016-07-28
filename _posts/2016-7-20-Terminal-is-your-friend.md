---
layout: post
title:  "Terminal is your friend"
---

------------------------------------------------------   The article is for MAC.

## What is terminal? #
![](http://cdn.appstorm.net/mac.appstorm.net/files/2012/02/Terminal-Home-cd.png)

In my opinion, terminal is the window that you can talk to the computer more directly  
and give orders to the computer. Computer only understands "0101..." binary system and ordinary people won't communicate with the computer using binary system which is tedious  and waste of time. So terminal allows users to communicate with more human instinct. All the commands are English-like and easy for human to understand. In the terminal, you can do literally everything that a mouse can do, you can have full control of the computer such as creating files, creating folders, opening files and so on. Terminal is a magic window!

## How to open a terminal? #
In MAC OS, you can simply go to `Launchpad` and then go to `other` folder, you can find terminal application under that folder.

Or you can use shortcut keys `command + space` which will lead to spotlight search. Then you can just type in `terminal` and hit enter.

If you don't want to do the steps above over and over again, you can just keep `terminal` in the dock. So every time you just need a click.


## Terminal can speak!!!#
Let's have some fun! If you have a mac beside, open your terminal and type in `say hello`, it will say it!

If you are not satisfied with the boring sound, you can change its style. Try `say -v cello hello`.

There are a list of voices mac can do, here's a [link](http://www.techradar.com/us/how-to/computing/apple/terminal-101-making-your-mac-talk-with-say-1305649). You can explore more on yourself with the fun.


## Terminal can do more!!! #
There are a lot of commands you can play around with your computer. Followings are the common ones.

### Terminal commands #

`pwd`

> show the current path you are in  

`ls`

> list contents in the directory

`ls -a`

> list all the contents including the hidden file in the directory

`ls -l`

> list contents in the directory as a list

`ls -la`

> just a combo of `ls -a` and `ls -l`

`cd`

> enter the desired directory  

For example: `cd filename`

`cd ..`

> go one level higher

`cd ~`

> go to home directory

`cd /`

> go to root directory. You can try the commands now and list all the contents under  
root directory and home directory, then you will see the difference between the home directory and root directory.

`mkdir & rmdir`

> make a new directory  &  remove an empty directory

`rm -rf`

> remove a directory with/without contents.(Be careful, no going back.)  

For example: `rm -rf directory_name`

`touch`

> create a file

`cat`

> get contents of  a file

`echo`

> add text to the file

For example: `echo 'text' >> hi.txt `

You can try all these commands in your terminal, it's fun!!!

### Useful hotkeys #

 `tab`

>However, if you want to go to somewhere deep inside your directory system, you will need some hotkeys. For example, you have a file in `~/the_history_of_Westeroes/the_children_of_the_forest_part/two_hundred_years_ago`, it would be very tedious to type in every word of the directory, now you can use `tab`, you only need to type in some part of the directory name, and `tab` will autocomplete the file path. You can first `mkdir` these fake example directory and `touch` a file under the `two_hundred_years_ago` directory. Now you can try to reach the file from root directory, you will find the benefit of using `tab`.

`Up and down arrow`

>Similarly, if you do not want to repeat your tedious command, when you type in command  in your terminal, just hit the arrow, it will review your command history.

`command + l`

>This will clear the terminal screen.

## Customize your own terminal #

#### Change  `preferences` #
**G**o to your terminal and set your preference!!
There is a [link](http://osxdaily.com/2013/02/05/improve-terminal-appearance-mac-os-x/) for your reference. There are more tutorials which are easy to get.

![](/assets/Screen Shot 2016-07-21 at 1.08.03 PM.png)


#### Change  `.bash_proflie`  #
**Y**ou can simply find and echo this file using what have been mentioned above. It is a hidden file in the home directory, if it does not exist, you can just create one also using what have been mentioned above. There are so many settings and you can explore yourself, following is an example for you to better understand how to manipulate with `.bash_proflie`

**G**o to your terminal, find your bash file, open it with nano.

![](/assets/Screen Shot 2016-07-21 at 1.43.03 PM.png)

**A**dd a line into the file. `export PS1=" [\u] \w💩 $ "`, it will show the difference.

![](/assets/Screen Shot 2016-07-21 at 1.57.10 PM.png)

**W**e Got it!!!

![](/assets/Screen Shot 2016-07-21 at 1.57.30 PM.png)

You may be wondering how can I put a poop inside, check the [link](http://osxdaily.com/2013/04/08/add-emoji-command-line-bash-prompt/)!!!
