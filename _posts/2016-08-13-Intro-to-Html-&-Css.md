---
layout: post
title:  "Intro to Html & Css"
---
------------- Show the world your ideas through internet

Before I ever went into the world of coding, I just found that some websites are beautiful, user-friendly and some are ugly and out of date. I never dig into that until I begin to understand how developers create a website from nothing. Now when I browse a website, I see differently. I can feel the bone and flesh, and the flesh is html and css.

##  Html   #
HTML is a markup language for describing web documents. HTML stands for Hyper Text Markup Language(No one cares but it is a good way to learn the nature of html). A markup language is a set of markup tags. HTML documents are described by HTML tags. Each HTML tag describes different document content. In my opinion, it is just a language that a browser understands, and it is made up. If you know the grammar and have enough vocabulary, you are good.

There are abundant resource for html, you can check out ([the link!](http://www.w3schools.com/html/default.asp)) . I will introduce some basics in case you are new to html.

You can try html on your own browser, it is easy. Just create a file with postfix ".html", double click it and you can see your page.

Try these lines below:

{% highlight html%}
<h1>Hello, world!</h1>
{%endhighlight%}

look what happened to your browser!

![]({{site.img_path}}/0813Intro_Html/1.png)

It is the begin of the magic ! I won't spend time on the grammar or vocabulary. So I will show you part of my code and it is easy to understand if you scan through the tutorial in [w3schools](http://www.w3schools.com/html/default.asp).

{% highlight html%}
<!Doctype html>
<html>
<head>
<title>Game of Thrones Tomblog</title>
</head>

<body>

<div class="title_image">
     <img src="http://vignette1.wikia.nocookie.net/gameofthrones/images/e/e5/Marc_Simonetti_Bran_theironthroneJoff.jpg/revision/latest?cb=20140926192518" alt="iron throne can not find" style="width:1200px;height:500px;">
     <h1><span>GAME of THRONES</span></h1>
</div>

<div >
	<ul>
		<li><a href= "#Home" >Home</a></li>
		<li><a href= "#History" >History</a></li>
		<li><a href= "#Houses" >Houses</a></li>
		<li><a href= "#Map" >Map</a></li>
	</ul>
</div>

<div class="background">
  <div class="title_history">
      <h2 id="History">History</h2> 	
  </div>
  <div class="Westeros_part">
      <p>WESTEROS<br>THROUGH<br>THE AGES</p>
  </div>

  <h3>The Dawn Age</h3>
  <p class="main_text">The children of the Forest were the first known inhabitants of<br>Westeros. Little is known of them, but lore describes them as<br>small
, druidic, and magical creatures. They worshiped the<br>gods of the nature and are believed to have carved faces in the<br>weirwood trees found across the continent.</p>
  <h3>Arrival of the First Men</h3>
  <p class="main_text">About 12500 years before Robert Baratheon took the iron<br>throne, a group of settlers crossed a land bridge from the<br>eastern continent of Essos into Westeros. Known as the first<br>men, these new arrivals' taming of the wilderness put them <br>at odds with the Children of the Forest and began a war that <br>lasted hundreds of years</p>
  <h3>The Age of Heroes</h3>
  <p class="main_text">After years of fighting, the Childeren of the Forest and the <br>First Men eventually reached an agreement known as the <br>Pact. They forged their alliance on the isle of Faces. The First <br>Men adopted the gods of their former enermies and lived in <br>harmony with the Children for many years.</p>
  <h3>The Long Night</h3>
  <p class="main_text">After one winter lasted an extremely long time and cold <br>settled across westeros, creatures known as the White <br>Walkers descended from the northern reaches of the continent. They attacked with ferocity, forcing the Children <br>and the First Men into the South, where the two peoples <br>finally rallied and drove their enermies back north, into the <br>Lands of Always Winter.</p>
  <h3>Kings of Westeros</h3>
  <p class="main_text">As a protection against future attacks by the White Walkers, <br>Brandon Stark-knowns as Bran the builder-erected a <br>massive ice wall across the northern boundary of Westeros. <br>The Night's Watch was founded to man the massive <br>structure's many strongholds. Brandon also established <br>Winterfell and began to rule as King in the North, while men elsewhere on the continent proclaimed themselves kings as <br>well. Soon, the people of the stormlands, teh iron islands, the <br>Rock, teh River and the hills, The Mountain and the Vale, the <br>Reach and the land of Dorne all lived under their own kings.</p>
  <h3>To be Continued</h3>
  <p class="main_text">......

  </p>
</div>

<div class="background">
  <div class="House">
     <h4 id="Houses">Houses</h4>
  </div>
  <div class="House_individual">
    <p><img class="House_symbal" src="http://assets.viewers-guide.hbo.com/larges1-houses-rgb-sigil-avatar-house-stark-1024x1024@2x.jpg" style="width:200px;height:180px;">
    <span class="House_name">House Stark<br></span><span class="House_motto"><br>Winter is coming<br></span></p>
  </div>
  <div class="House_individual">
    <p><img class="House_symbal" src="http://assets.viewers-guide.hbo.com/larges2-houses-rgb-sigil-avatar-house-baratheon-joffrey-1024x1024@2x.jpg" style="width:200px;height:180px;"><span class="House_name">House Baratheon<br></span><span class="House_motto"><br>Ours is the fury<br></span></p>
  </div>
  <div class="House_individual">
    <p><img class="House_symbal" src="http://assets.viewers-guide.hbo.com/larges1-houses-rgb-sigil-avatar-house-targaryen-1024x1024@2x.jpg" style="width:200px;height:180px;"><span class="House_name">House Targaryen<br></span><span class="House_motto"><br>Fire and blood<br></span></p>
  </div>
  <div class="House_individual">
    <p><img class="House_symbal" src="http://assets.viewers-guide.hbo.com/larges1-houses-rgb-sigil-avatar-house-greyjoy-1024x1024@2x.jpg" style="width:200px;height:180px;"><span class="House_name">House greyjoy<br></span><span class="House_motto"><br>We do not sow<br><br></span></p>
  </div>
  <h3>To be Continued</h3>
  <p class="main_text">......



  </p>
</div>

<div>
  <h4>Map</h4>
  <div class="map_west"><img src="http://vignette2.wikia.nocookie.net/gameofthrones/images/7/7e/The_known_world_HBO.jpg/revision/latest?cb=20130507121142" style="width:1280px;height:760px;"></div>

</div>

</body>
</html>
{% endhighlight %}

It is kind of overwhelming, and you don't need to understand it immediately. You can just scan the code and know some content types, have a general vision of the page, that's all. You can dig in if you have enough time.

##  Html & Markdown #

So programmers are lazy, they always want it more convenient to code. They always design the coding language more like English for humans to understand. So there is markdown language for html.

Markdown is a lightweight markup language with plain text formatting syntax designed so that it can be converted to HTML and many other formats using a tool by the same name. So how does it work? It is like a bridge between html and the plain text, so people only needs to put in English-like text and symbols, it will convert these into html that the browser understands, then people don't have to remember all those tags and formatting.

Here's a markdown [cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).
Below is what it looks like. Its nature is html.

{% highlight markdown%}
An h1 header
============

Paragraphs are separated by a blank line.

2nd paragraph. *Italic*, **bold**, and `monospace`. Itemized lists
look like:

  * this one
  * that one
  * the other one

Note that --- not considering the asterisk --- the actual text
content starts at 4-columns in.

> Block quotes are
> written like so.
>
> They can span multiple paragraphs,
> if you like.

{%endhighlight%}

You can tell that it is more English-like and more coder-friendly.
There are tons of other similar softwares like Markdown, but main features of those softwares are the same. You only need to adapt to their syntax, that's all.

##    Css    #

Cascading Style Sheets (CSS) is a style sheet language used for describing the presentation of a document written in a markup language. Although most often used to set the visual style of web pages and user interfaces written in HTML and XHTML, the language can be applied to any XML document, including plain XML, SVG and XUL, and is applicable to rendering in speech, or on other media. Along with HTML and JavaScript, CSS is a cornerstone technology used by most websites to create visually engaging webpages, user interfaces for web applications, and user interfaces for many mobile applications.

In conclusion, Css is like makeups, so I will show you the power of it.  

Below is the html without the css.

![]({{site.img_path}}/0813Intro_Html/2.png)

Here is the html with makeups!

![]({{site.img_path}}/0813Intro_Html/3.png)

![]({{site.img_path}}/0813Intro_Html/4.png)

How does this magic work? Still a bunch of codes.

{% highlight css %}

h1 span{
	color: black ;
	font: bold Helvetica, Sans-Serif;
	letter-spacing: 1px;
	background: rgb(0,0,0);
	background: rgba(0,0,0,0.4);
	padding: 25px;
}
.title_image {
	position: relative;
	display: block;
	margin: auto;
	width: 80%;
}
h1 {
	position: absolute;
	top: 355px;
	left: 0px;
}
ul {
	list-style-type: none;
	margin: 0;
	padding: 0;
	overflow: hidden;
	background-color: #444;
}
li {
	float: left;
}
li a {                      /*-- I want to change font-style but it just do not work -->*/
	font-size: 20px;
	display: block;
	color: white;
	text-align: center;
	padding: 20px 40px;
	text-decoration: none;
}
li a:hover {
	background-color: #111;
}
h2 {
	font-size: 30px;
	border-bottom: 3px solid grey;
	text-align: center;
	padding-bottom: 35px;
	padding-top: 100px;
}
.background{
	background-color: #DCDCDC;
}
.title_history {
     padding:20px 400px 5px 400px;
}
.Westeros_part {
	font-size: 50px;
	text-align: center;
}
h3 {
	font-size: 25px;
	text-align:left;
	padding: 0px 505px 0px 505px;
	font-family: Tahoma, Geneva, Sans-Serif;

}
.main_text{
	line-height: 1.8;
	text-align:center;
	font-size: 20px;
	text-align:left;
	padding: 0px 400px 0px 505px;
}
.House {
	padding:20px 400px 5px 400px;
}
h4 {
	font-size: 30px;
	border-bottom: 3px solid grey;
	text-align: center;
	padding-bottom: 35px;
	padding-top: 100px;
}
.House_symbal {
	float: left;
	margin: 20px;
}
.House_individual {
	padding: 40px 0px 40px 100px;
}
.House_name {
	font-size: 45px;
	font-weight: bold;
	letter-spacing: 3px;
	word-spacing: 0px;
	text-align: center;

}
.House_motto {
	font-size: 40px;
	text-align: center;

}
h4 {
	font-size: 30px;
	border-bottom: 3px solid grey;
	text-align: center;
	padding-bottom: 35px;
	padding-top: 100px;
}
.map_west {
	display: block;
	margin: auto;
	width :90%;
}

{%endhighlight%}

Don't panic! They are just made up like html, it is easy when you know the syntax.
Check out the [resource](http://www.w3schools.com/css/default.asp)!

Again, programmers are smart(lazy)! There are many libraries, softwares available. You only need to choose what you like and copy and paste!

For example, [**Bootstrap**](http://getbootstrap.com/)!
It's just like an online store for the styles you want to apply for your website or project.

![]({{site.img_path}}/0813Intro_Html/5.png)

I will not dig in, it's your turn now!
