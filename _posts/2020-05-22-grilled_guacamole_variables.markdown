---
layout: post
title:      "Grilled Guacamole variables"
date:       2020-05-22 21:03:31 -0400
permalink:  grilled_guacamole_variables
---


Class variables and instance variables were a big part of my project . The biggest question was  choosing when would be the right time to use them within the scope of Objective Orientation .In my CLI project I  maneuvered between them to be able to help the user navigate their cravings.
 
 
Class variables are the same value  across all class instances.  They are preceded by the sign @@ and are followed by the variable name.Class variables are also available to both instance methods and class methods. These variables can be used to store data that belongs to a class, but not to its instances. In Foodies, my Dish class I present @@all = [] which you can determine the many number of objects that are being created. 

```

class    Dish

	  attr_accessor :name, :dish_id , :cuisine , :sum
	

	  @@all = [ ]
	

	  def initialize (name:, dish_id:, cuisine:, sum:)
	    @name = name
	    @dish_id = dish_id
	    @cuisine = cuisine
	    @sum = sum
	    @@all << self
	  end
	

	  def self.all
	    @@all
	  end
	  def self.find_by_cuisine(cuisine)
	    self.all.select {|dish| dish.cuisine == cuisine}
	  end
	end
```
	

Instance variables are available across methods for any instance or object. That means that instance variables change from object to object. It gives them attributes or properties and teaches them that this data defines them. While normal variables can  only be called in a method if they are passed in as an argument, instance variables have the added ability to be accessed by instance methods of a particular class using object orientation, defying the conventional limitations of the local scope. Instance variables are preceded by the at sign (@) followed by the variable name.





  ```
	def print_dishes(dishes)
	    sorted_dishes = dishes.sort_by_length
	    puts "~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ "
	    puts "Here are some  #{@cuisine} dishes."
	    sorted_dishes.each.with_index(1) do |dish ,index|
	      puts "#{index}. #{dish.name}  #{dish.dish_id}"
	    end
	    puts "~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ "
   end

```




Within my class CLI  file above , I decided to use an instance due to  its ability to communicate with my Dish file .This gives me the ability to access the information of the different cuisine dishes  and present them to the user. The instance variables I chose were better alternatives than class variables due to  the data not sharing across the inheritance chain shared by the Class and subclasses.

In conclusion, my usage of Class and Instance variables made it possible to have  the ability to take advantage of the inheritance chain  of Class variables  and to navigate outside of it. This made it possible to supply the users with delicious dishes from all over within seconds. 


