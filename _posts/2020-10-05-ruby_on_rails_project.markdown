---
layout: post
title:      "Ruby on Rails Project"
date:       2020-10-05 20:01:38 -0400
permalink:  ruby_on_rails_project
---

This was one of the more enjoyable projects so far.  

In this mod we were tasked with gathering all the tools and systems we have learned so far and build an app that displays our working comprehesion of each process. 

Using ruby methods and structure I created an app that will provide information on games with details about how many players can play the game, What kind of game is it? Is the game fun to play with a group of people or is it more focused on a single player? Is the game able to be played with friends and family under the same roof or can you play remotely?

I call my application "Family Game Night". I put this project togehter because over the last year or so my family and I have been having fun playing games remotely and I wanted to learn about other games that could be fun for us to try.

I started with my controllers. First was the reviews controller. Here users can give reviews of the games and give thier experience playing them. Not only can a user leave a review on a certain game but the user can also edit and delete their review is they want to. It is also possible for a user to see not only all the reviews posted by all the users but also narrow it down to just the reviews they have posted. With this option came the task of making sure only said user can edit and delete reviews if they happen to be the user that created them.
The reviews controller connects the other two controllers for the users and the games.

The games handles all the game information that is added to the application. Here the game has a few attributes that help to identify the games for the users. You are prompted to give data in regards to genre, theme of the game, how many players is the game and of course a description of what the game is about.

Users must create an account before they are given access to any of the data in the application. Once an account is created, a user can skim the game library and check out all the reviews from other users to help them find the perfect game for them to play with their friends and family. The best part is that a user can add thoer own games that they have had fun playing and hopefully other users will be able to find some joy from those games as well.

Ruby on rails is not really a programming language but more of a neatly packaged shell that contains some very nice "magic" or shortcuts in the ruby language.  Maybe it is better to call it a template. This template is nice because it helps keep things seperate and clean in regards to the code. I found it helpful to think of it as having a compartment for everything. When working on the seperation of concerns rails makes this easy but not effortless.  There is a lot of data available and for a beginner such as myself weeding through all the files can be a challenge in of itself. I focused on the core files and directories and of course google was a great help for the questions I came across while building this app.

As I was building the controllers out with code to do each function I was creating, I also was matching up the "views" files. The views is where all the code comes to life and becomes accessible to the users. This takes some knoweldge of HTML and CSS if you want to format and make it pretty.  This is where I was able to delevop the forms that the users can fill out to create  game details and reviews. The forms take that data and store it to be used at a later time when it is called on.  The veiws also provide a user interface and allow the user to indirectly interact with all the code in hte controllers.

For each controller ie.. users, reviews and games there is a corrosponding view or multiple views depending on what code was written. For example if the code says to modify data, there will be a view named "edit".  For the actions that provide a "new" instance like creating a new user or entering a new game or review to the data base the view is typically labeled "new" and of course to bring it all togehter and display the data to the user it will be displayed through the "show" view.

This process includes the DRY (Dont Repeat Yourself), MVC (Model-View-Controller), RESTful and CRUD (Create-Read-Update-Delete).  All were used in the creation of this Family Game Night Application.
