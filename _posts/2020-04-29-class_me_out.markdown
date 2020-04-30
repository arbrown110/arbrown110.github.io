---
layout: post
title:      "***# Class me out!!***"
date:       2020-04-30 01:34:56 +0000
permalink:  class_me_out
---




 
 
As I learn, I call it my road to the outlet. This is because before you can plug into something you must first find the socket. Without that socket you must search for a way to get the power to charge your plug.  
 
Class variables and methods are pulling me to understand the wires that form the cord to many of the plugs I need. The use of variables and methods within a Class help me learn about the functionality of the Class. 
 
**Class Variables** store information regarding the class. 
      	**Class Methods** enact behaviors that belong to the whole class, not just to the individual instances of that class. 


Class variables are written with double (@@) at symbols, like local and instance variables you can set it equal to data. Yet you can only access the information outside of the class with building a Class Method to hold it. 
 
**Class Variable**                                                      
 ```
 class Album  
   @@ album_count = 0 
  
	 def release_date = (data) 
     @release_date = data 
    end 
 
    def release_date 
      @release_date 
    end 
  end 
 ```
 **Class Method **
 ```
  class Album 
   @@album_count = 0 
 
   def self.count 
     @@album_count 
   end 
  end 
 ```

Which will allow us to call  **Album.count**  that gives us **0 **

Now I'm able to know how many albums I can find my database. I'm also able to build more methods that will allow me to do more with the class. 


