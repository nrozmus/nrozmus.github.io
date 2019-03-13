---
layout: post
title:      "Rails Final Project For FlatIron"
date:       2019-03-13 00:29:44 -0400
permalink:  rails_final_project_for_flatiron
---


The Gambling Hotels application was built with the intention of being a content management system for two select hotels found at casinos. These casino's are Jake's 58 on Long Island and Mohegan Sun in Connecticut. Inspiration for this came from my local interests in blackjack, with a bet always made to my friends that if we win big, we will book a hotel for the night and enjoy ourselves for another day. Although that day has not come yet, this is a mock hotel reservation app that runs on Ruby on Rails. It offers rooms from two different and popular casino hotels at current prices. Once you have registered, either through my site or GitHub, you can reserve as many rooms as you want, as long as that room type is available.

Here are the steps I used to create my project application.

1-**Creating the Application**

To create files with Rails just type on the terminal:

**$ rails new app_name**

2- **Install the Required Gems**

By default Rails applications manage gem dependencies with Bundler. 

I added the gems below to my gemfile.

gem ‘omniauth’
gem ‘omniauth-github’
gem ‘dotenv-rails’
gem ‘pry’
gem ‘bycrypt’

Run bundle:

$ bundle_install

**3-Create the Database**

Example of a table to create a hotel reservation.

![]((https://i.imgur.com/TEqgLTN.png))

Use a rake command to run the migration:

$ rake db:create


4- **Create Models**


Here is an example of my app/models/user.rb file. I have added validations and to secure a password, I included the gem bcrypt in my gemfile .

The **has_secure_password** adds methods to authenticate against a BCrypt password. This mechanism requires you to have a **password_digest attribute**. This is create to secure your app if you are not using gems to secure your app.

![]([Imgur](https://i.imgur.com/cplRv22.png))


These validations will ensure that users have a name, password and that they can have many reservations, addresses and rooms.

**5- Create Views**

Remember that views directly interact with the user. This is where I put all the code that makes my app look great, and how my user sees and interacts with it . Here is an example of the topics view folders.
![]([Imgur](https://i.imgur.com/cLGfokf.png))

**6- Create Controller**

It’s the brains of the application, and ties together the model and the view. Here is where all the actions code goes. 

![]([Imgur](https://i.imgur.com/6NrQsJe.png))

**Final Product**

![](https://i.imgur.com/aq9yqAN.jpg)


Remember to utilize your resources, google is a wealth of knowledge. You don't have to know how to do *every little thing* and you can save a ton of time and debugging work by visiting popular coding sites such as Stackoverflow or Github. Don't be afraid to ask questions or get help, whether it's here, a friend, or even a stranger on the internet. Remember that what makes the coding community a powerful force is the open source of most code, allowing not just one person to contribute, but everyone as a whole. That's how technology moves so fast, it's how many new products and software come out (refactoring and rethinking existing code, creating new ideas, etc).  Happy coding!


