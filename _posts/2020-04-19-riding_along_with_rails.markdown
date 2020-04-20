---
layout: post
title:      "Riding Along with Rails"
date:       2020-04-20 03:18:30 +0000
permalink:  riding_along_with_rails
---



For my Rails project I decided to create a Computer building app. My app allowed a user to create orders and multiple computers and add them to the orders. This Rails project was a turning point for me , it was where everything I have learned up to this point was finally coming together .Everything from the Cli project to Sinatra,  and Sinatra to Rails  seemed to build on each other. I was able  to use the lessons I learned to figure out solutions to almost every problem I ran into, and boy did I run into a lot of problems. This project more than any gives you the tools to solve almost everything. Rails is literally like magic. I'm going to list some of the problems I ran into .


The first problem I ran into was that I didn't have yarn installed on my computer. With the help of stack exchange I figured out that I needed  to go to  https://classic.yarnpkg.com/en/docs/install#windows-stable to install the updated version of yarn, and run this command:

`rails webpacker:install `

The second problem i ran into was now I had to figure out how I wanted to set up my many to many associations for my project. half way through my project i realized that my association were not connecting.I ended up having to redo my associations and I decided on 

`class User < ApplicationRecord
   has_many :orders
   has_many :computers
   has_many :ordered_computers, through: :computers, source: :order
	end`
 
 
 `class Computer < ApplicationRecord
    belongs_to :user
    belongs_to :order
	end`
	
	`class Order < ApplicationRecord
	  belongs_to :user
    has_many :computers, :dependent => :destroy
    has_many :users, through: :computers
	end`
	

The dependent => destroy method was added later so that I could delete a parent object of order and the child object of the computer.The associations were difficult for me to grasp at first I had to figure out how my program would flow through each model. I had to make sure I had the right keys on each table and I was able to use the belongs_to macro to associate tables and set foreign keys. Once my migrations were set up and I got to the controllers and views I was able to really see the magic of rails. I was able to user helper methods such as redirect_if_not_logged_in , logged_in? , and current_ user to make my controller more DRY.

The third problem I ran into was creating a new object in the new and create action. When I instatiated an object with. new i was not to associate an parent object with a child object. The build method is also another cool method that allowed me to instantiate an object that was already assocaited with another object.

` @computer = current_user.computers.build(computer_params)`

After getting past the problems and using rails resources and learn lessons I was able to make more progress on my project. One of the coolest features of my project was including the ability for a user to log in using Google. Omni auth allowed me to take a user credentials and match them to my database and log them in.This feature allowed more functionality of my app. Knowing how to use Google developer tools and how to create an app was also a fun learning experience.

One of the main things I learned was that coding is not only about being able to remember information but being able to look things up and using the rails community to figure things out. I got the sense that the rails community is a team and everyone plays their part. I was able to get parts of my code working by looking up documentation and finding information on stock exchange.I look forward to working with rails in the future and I appreciate its level of accessibility.

 
 
	 
	 

