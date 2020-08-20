---
layout: post
title:      "Sinatra/REST/CRUD/MVC Project"
date:       2020-08-06 14:54:13 -0400
permalink:  sinatra_crud_mvc_project
---


Here I will discuss the process of creating an application using the CRUD and MVC processes through Sinatra.  Sinatra is a nice tool that helps set up your repo with most of the goodies you will need to structure your idea into a working application.  

I used active record to organize and manage all the data the user will be entering from the terminal and the CRUD process to make managing that data a bit easier. The process of diving up tasks is given to a process called MVC or Model/View/Controller. This is a divide and conquer technique that prioritizes tasks making it easier to write code and easier to understand code that someone else has written.

The idea seems simple enough and setting this up went pretty smooth.  I found this project to be challenging at times and also rewarding. 

The blue print and concepts are all there, making it flow and communicate seems like a paint by numbers version of coding but it was a lot more than that. Systems like RESTful and CRUD give you the basics as far as structuring your code. The rest is on you or me for this project. 

First I'll talk about REST or Representational state transfer. Rest is a software architectural style that defines a set of constraints to be used for creating web services, building applications or websites.  Ok, that is probably the most techincal sounding sentence I will be putting in this entry.  If you remeber from some of my very first posts how I said I have had zero exposure to programming, I am still not that comfortable with the language.

The link below will take you to a basic REST table that is a good example of the process I used:

![](http://)https://www.google.com/url?sa=i&url=http%3A%2F%2Fwww.restular.com%2Fabout.html&psig=AOvVaw39-cGRYAwmHZR7RridPSps&ust=1598043739650000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCNjH5P3WqusCFQAAAAAdAAAAABAv

The think the actual process is pretty complex but can also be simplified by understanding that as code is written there is a certain flow.  In REST, you have routes. These routes are written similarly to Ruby methods including the "end".  My project is basically an inventory app.  A user can create an account and add, edit and delete items they want to store in thier virtual vault.  The application will not allow an email address to be used more than once and it will not allow a user to snoop on other users stuff.

I will list a couple of the REST route I used and what they do:

The **'/get'** route as you can see on the table I shared above, is known as the "index action" and is used to direct the code to an index page which should display the current_user's list of stuff or as I call it in my application, the user"s "vault". I added code to the users_*controller* file that makes sure the user is actually logged in and if they are not it will navigate them to the login page so they can log in.

If the user is does not have an account they can click "create_account" and a different **GET** request **'/signup'** will take them to a signup page where they can create an account. 

After providing a password, username and email the user will click the "create" button and then my** POST** request does some fact checking..  **post '/signup'** validates that the email provided has not already been used on another account and if it is a new email, directs the new user to their empty "vault" where the user is given a couple options on what to do next.

The user is offered a couple different things next, are we adding new items to the vault? Are we deleting things that are currently in the vault? Or are you just wanting to update something you already entered?  The route used depends on the the choice the new user decides. 

User wants to add new items to the vault: 
A GET request is made and a** POST** request validates the user did his job and then adds the item to the vault while assigning an :id to the item so it can be found later.

User wants to update his items:
A get request is made and a **PATCH route **validates that the item is in the vault and belongs to the user requesting it. 

Routes are used to login and logout , update and delete. But this is just one step in the whole process of building this application. We still need to cover CRUD and MVC!  But that will have to wait for next time.





