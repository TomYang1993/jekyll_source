---
layout: post
title:  "Flashes (sessions cont.)"
---

##  Cookies  #
  In last post, we have talked about how to keep data between requests, but not clear about  
  the relationship between cookies and sessions. Cookies are key-value data pairs that are stored in the user's browser until they reach their specified expiration date. Cookie can be interpreted as a special hash. It is attached on every web request and carries on mostly user's info.

  In rails, according to my search, sessions and cookies don't have much difference. Rails work with cookies to make it more secure. The info is still stored as a hash in the cookies, so user puts in some data in the cookies, and then rails app extracts that data. Sessions are like some part of the cookies.

  Of course, there are other ways to store the data in sessions, check the [link](http://www.justinweiss.com/articles/how-rails-sessions-work/)

## Sessions and Flashes  #
Sessions are not hash in nature, session just act like a hash. It is a method and rails pretend it is a hash and then programmers are easy to work with. To better understand sessions, let me introduce his brother, flash!

Normally when you purchased a product, there would be a message showing successful purchase(no matter in what form). And then when you refresh the page, it would disappear in just a flash. You must be familiar with this situation. That's a flash message!

![](http://assets.materialup.com/uploads/f03c6dc2-389d-4122-ae4f-9efb13294d8d/03d17e30671583.562e33d4c8f75.png)

Session and flash are very similar, except that flash can **only last one request**! From last post, we know that session can last many requests until user close the browser or sign out. But flash can only last one request, **it will be wiped out in the next request!**

## Flashes in rails #
There exists a generic system to show users that an action was performed successfully, or more importantly, failed. This system is known as "flash messages".
Normally, we set up flash message in the `application.html.erb` above the `yield` section.

{% highlight html%}
 <%=  flash.each do |name,message|%>
   <%= message %>
 <% end %>
{% endhighlight %}

Then set up the flash hash in the controller or model to take in the info and type of the flash message.

{% highlight ruby%}
 flash[:success] = "The system has been successfully updated !"
 flash[:danger] = "Your purchase is not successful !"
 flash[:warning] = "Are you sure to delete this item ?"

{% endhighlight %}

Usually, flash message pairs with redirection, and the flash message will be shown on the page you direct to.

When we deal with validations, error messages can be a lot, so message attribute of the flash can be an array. So we have to adjust flash both in the view and controller.

{% highlight html%}
<% flash.each do |name, message| %>
   <div class="alert alert-<%= name %> alert-dismissible" role="alert">
     <button type="button" class="close" data-dismiss="alert" aria-label="Close"><span aria-hidden="true">&times;</span></button>
     <% if message.is_a?(Array) %>
      <ul>
       <% message.each do |msg| %>
        <li>  <%= msg %>  </li>
       <% end %>
     </ul>
     <% else %>
     <p> <%= message %> </p>
     <% end %>
   </div>
<% end %>
{% endhighlight %}

{% highlight ruby%}

 flash[:danger] = @product.errors.full_messages

{% endhighlight %}
