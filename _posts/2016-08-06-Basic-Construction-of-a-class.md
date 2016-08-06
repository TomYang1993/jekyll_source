---
layout: post
title:  "OOP basic construction"
---

> An object is an entity that serves as a container for data and also controls access to the data. -- Hal Fulton

## Initialize Method #

When we are doing Object Oriented Programming(OOP) style，we usually create a class, and a class  
should be initialized to give attributes values and gain access to attributes.

A class is like a factory, when creating a new instance, it will give it a unique ID, just like goods has tags. Inside a class, there is a method called initialize to give values to these newly created instances.

For example, there is a luxury-car factory:

{% highlight ruby %}
class Luxury_car
  def initialize

  end
end

luxury_car = Luxury_car.new
#=> An instance created but not initialized
{% endhighlight %}

If we want to give more specific attributes to the class, we could pass in arguments in the initialize method.

{% highlight ruby %}
class Luxury_car
  def initialize(make, model, year)
    @make = make
    @model = model
    @year = year
  end
end

luxury_car = Luxury_car.new("Lanborghini", "Aventador", "2012")
#=> We are using @ here to get access to the variable through the class.
{% endhighlight %}

Now we give the instance variables values, but we still can't extract the info from the class, so we need a getter method to get the info.

## Getter and Writer Method #

{% highlight ruby %}
class Luxury_car
  def initialize(make, model, year)
    @make = make
    @model = model
    @year = year
  end

  def make
   return @make
  end

  def model
   return @model
  end

  def year
   return @year
  end
end

luxury_car = Luxury_car.new("Lanborghini", "Aventador", "2012")
p luxury_car.make
p luxury_car.model
p luxury_car.year
#=> Now we can call method on the instance to get the info.
{% endhighlight %}

**H**owever, when the scale of the attributes gets bigger, every attribute needs a getter method, so 10 attributes need 10 methods, 100 attributes need 100 methods, that pain won't end.  

What's more, when we want to write values to attributes, we need a writer method, so 10 attributes need 10 writer methods, so in total we need 20 methods to fully access the attribute, that will be more pain.

Luckily, programmers are lazy, and programmers always get a way! `attr_reader` will help!

{% highlight ruby %}
class Luxury_car
  attr_reader :make, :model, :year
  def initialize(make, model, year)
    @make = make
    @model = model
    @year = year
  end
end

luxury_car = Luxury_car.new("Lanborghini", "Aventador", "2012")
p luxury_car.make
p luxury_car.model
p luxury_car.year

#=> Now we dry up the code.
{% endhighlight %}

What does a writer method look like ?

{% highlight ruby %}
class Luxury_car
  attr_reader :make, :model, :year
  def initialize(make, model, year)
    @make = make
    @model = model
    @year = year
  end

  def make=(make_value)
   @make = make_value
  end
end

luxury_car = Luxury_car.new("Lanborghini", "Aventador", "2012")
p luxury_car.make
p luxury_car.model
p luxury_car.year
luxury_car.make = "Porche"
p luxury_car.make

#=> Now we can manually type in the make of a car instance
{% endhighlight %}

Remember programmers are lazy! `attr_writer` will help !


{% highlight ruby %}
class Luxury_car
  attr_reader :make, :model, :year
  attr_writer :model, :year
  def initialize(make, model, year)
    @make = make
    @model = model
    @year = year
  end
end

luxury_car = Luxury_car.new("Lanborghini", "Aventador", "2012")
p luxury_car.make
p luxury_car.model
p luxury_car.year
luxury_car.make = "Porche"
p luxury_car.make
luxury_car.year = "2010"
p luxury_car.year
{% endhighlight %}

We can dry up our code more with `attr_accessor`!

{% highlight ruby %}
class Luxury_car
  attr_reader :model
  attr_accessor :make, :year
  def initialize(make, model, year)
    @make = make
    @model = model
    @year = year
  end
end

luxury_car = Luxury_car.new("Lanborghini", "Aventador", "2012")
p luxury_car.make
p luxury_car.model
p luxury_car.year
luxury_car.make = "Porche"
p luxury_car.make
luxury_car.year = "2010"
p luxury_car.year
{%endhighlight%}

You should try to run all the files above in the terminal to see the difference.

## Extras: more tips for drying up your code #
Now we are passing in three arguments into our car class, say if we want to pass in seven arguments into the car class, like the number of cylinders, the position of engine etc. We have to memorize the order of the arguments to pass in different values with different data types, we are humans, we will make mistakes. So pass in a hash is a good way!

{% highlight ruby %}
class Luxury_car
  attr_accessor :make, :year, :model
  def initialize(input)
    @make = input[:make]
    @model = input[:model]
    @year = input[:year]
  end
end

luxury_car = Luxury_car.new(make: "Lanborghini", model:"Aventador", year: 2012)
p luxury_car.make
p luxury_car.model
p luxury_car.year
{%endhighlight%}

So now you don't have to worry about the type or order of the arguments.
