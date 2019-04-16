---
layout: post
title:      "Rails w/ JS frontend project"
date:       2019-04-16 23:36:55 +0000
permalink:  rails_w_js_frontend_project
---


I decided to update my previous rails project for this assessment. It is an app that allows you to book hotel rooms and decide on check-in/out times. Adding Javascript to this allowed for less page refreshes and a more dynamic feel. I also implemented reviews that you could read about the rooms all while without refreshing the page. The JS was added in areas of the application where it could improve the overall UX by means of manipulating the DOM. This improved the speed at which data was loaded on to the page, and another area where the user can submit data to the database if need be.
![](https://static.makeuseof.com/wp-content/uploads/2017/04/Tech-News-Windows-Update-Pause-Button-670x335.jpg)

Project requirements were the following:

1. Make use of ES6 features (Arrow functions, const, let, etc…).
2. Render at least one index page dynamically
3. Render at least one show page dynamically
4. Render at least one has_many relationships to the page
5. Must use the Rails app to render a form for creating a resource that is dynamically submitted using JS
At least one of the JS models must have a method on prototype

Although easier than building the rails app itself, I still felt adding this layer ontop of what existed caused a lot of issues. It's hard going from such a programmer-friendy language and switching to Javascript which I admit seems much less intuitive. There are a lot of odd things that can happen when you mess up and I spent a lot of time researching and sorting out why things were not working the way they were supposed to. Overall it's a very useful language but I'm curious as to what the future will hold for it.
