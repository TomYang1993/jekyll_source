---
layout: post
title:  "Sessions(cont.)"
---

##  Cookies  #
  In last post, we have talked about how to keep data between requests, but not clear about  
  the relationship between cookies and sessions. Cookies are key-value data pairs that are stored in the user's browser until they reach their specified expiration date. Cookie can be interpreted as a special hash. It is attached on every web request and carries on mostly user's info.

  In rails, according to my search, sessions and cookies don't have much difference. Rails work with cookies to make it more secure. The info is still stored as a hash in the cookies, so user puts in some data in the cookies, and then rails app extracts that data. Sessions are like some part of the cookies.

  Of course, there are other ways to store the data in sessions, check the [link](http://www.justinweiss.com/articles/how-rails-sessions-work/)

## Sessions and flash  #
Sessions are not hash in nature, session just act like a hash. It is a method and rails pretend it is a hash and programmers are easy to work with. To better understand sessions, let me introduce his brother, flash!

When you purchased a product, there would be a message showing successful purchase(no matter in what form). And then when you refresh the page, it would disappear in just a flash. You must be familiar with this situation. That's a flash message!

![](http://assets.materialup.com/uploads/f03c6dc2-389d-4122-ae4f-9efb13294d8d/03d17e30671583.562e33d4c8f75.png)

Session and flash are very similar, except that flash can only last one request! From last post, we know that session can last many requests until user close the browser or sign out. But flash can only last one request, it will be wiped out in the next request!
