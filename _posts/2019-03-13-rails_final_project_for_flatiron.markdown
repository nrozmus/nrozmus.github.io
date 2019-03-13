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

![](https://imgur.com/TEqgLTN.png)


