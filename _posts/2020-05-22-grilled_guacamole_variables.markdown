---
layout: post
title:      "Grilled Guacamole variables"
date:       2020-05-23 01:03:30 +0000
permalink:  grilled_guacamole_variables
---


Class variables and instance variables were a big part of my project and choosing when would be the right time to use them within the scope of Objective Orientation .In my CLI project I danced within the two to be able to help the user navigate their cravings.


Class variables are available across different objects. A class variable belongs to the class and is a characteristic of a class. They are preceded by the sign @@ and are followed by the variable name. In Foodies, my Dish class I present @@all = [] which you can determine the many number of objects that are being created. 

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
	    sorted_dishes = dishes.sort_by{|dish|[dish.name.length]}
	    puts "~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ "
	    puts "Here are some  #{@cuisine} dishes."
	    sorted_dishes.each.with_index(1) do |dish ,index|
	      puts "#{index}. #{dish.name}  #{dish.dish_id}"
	    end
	    puts "~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ "
   end

```




Within my class CLI  file above , I decided to use a instance due it’s ability to communicate with my Dish file .This gives me the ability to access the functionally of the different cuisine dishes  and present them to the user. As we know normal variables cannot and class variables would more than just @cuisine. A class variable would give too much of the information at one time, making it impossible to give the user exactly what they are looking for when the user is just looking to utilize one object within the system.

In conclusion, my usage of Class and Instance variable made it possible to have  the ability to be shared among the class with all of it’s descendants from the parent class  and to have the  ability to have separate instance where it is not shared.

