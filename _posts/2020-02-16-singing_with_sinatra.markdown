---
layout: post
title:      "Singing With Sinatra"
date:       2020-02-16 14:32:24 +0000
permalink:  singing_with_sinatra
---

**Beginning**
     I just completed my second project using Sinatra, and I'm feeling a lot more confident in my abilities. Just like my Cli Project I was not sure where to start. I decided to think of the project like creating a song. I had to break it down into break the project down into steps and not think of it as a whole application until I completed it. First thing I did was run the corneal gem to give me a base application to start with. I remembered the acronym MVC , which stands for models,views and controllers. I had decided to create an app that allows a user to store a list of their favorite video games. I began my journey by creating my migration tables and some seed data for my database, then I migrated them to my database.

Now what's next...


**Models**
   Creating the models was the next step in creating my app. This is where I put my logic. ActiveRecord made it really easy for me, I didn't have to create any initialize methods or attribute accessors because ActiveRecord came with pre built methods. I had two clases my user class and my game class.I associated my user class with my game class by using "has_many" and "belongs_to" .The game class belongs to the user class. I also included a user id to join my tables with a foreign key. 
	 
	 
**Views**
   I had the most fun with the views part of my application because as I manipulated the HTML,  I could actually see the changes i made on the web page.Whenever I added a form or a link I would see it appear on the web page like magic. I added a little CSS styling but I have a lot more to learn. There are so many different possibilities with CSS, I can see that it can take a while to master.
	 
	 
**Controllers**
   In my controllers I put my http routes. There are 5 main restful routes. Get,Post,Patch,Put and Delete.These routes allow mapping between http verbs and and CRUD functions.I spent the most time writing code in my controller files.


**Getting It to Work**
   I fired up shotgun and my webpage appeared. I was able to create a user and create,read, update and destroy game entries for that user. The hardest part about the project was making sure that each user only saw their entries and not another users entries.I used my helper methods "logged_in?" and "current_user". I learned that helper methods are very useful in creating clean DRY code that doesn't repeat itself. 
	 
	**On To Bigger and Better Things**
	 Now that I have submitted my Sinatra project I'm really excited to see what's next. I'm at the middle ground, where I'm starting to feel more confident but I'm still not sure if I have what it takes to be a software engineer. Hopefully I have what it takes, and I am going to give it everything I've got.
	 

