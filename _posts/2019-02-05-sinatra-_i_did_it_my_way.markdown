---
layout: post
title:      "Sinatra- I Did It My Way!"
date:       2019-02-06 04:57:34 +0000
permalink:  sinatra-_i_did_it_my_way
---


I've loved, I've laughed and cried

I've had my fill, my share of losing

and now, as tears subside

I find it all, all so amusing

![](https://www.biography.com/.image/ar_1:1%2Cc_fill%2Ccs_srgb%2Cg_face%2Cq_auto:good%2Cw_300/MTE4MDAzNDEwNjg4MTE2MjM4/frank-sinatra-9484810-3-402.jpg)

A legendary song by Frank Sinatra, the first thing that came to mind when I worked with this program. The lyrics, also witfully suitable to my experience with the project! There were moments of joy as things began to work, and also boiling points hit when one thing would break and you would spend 5+ hours scouring the internet for solutions, reaching out to your cohort, technical help, etc. It's tough, there's a lot of integrations that take place, getting your models to interact with one another, perfecting your MVC's, etc.

**But let's get to it!**

# App Requirements:
# Specifications for the Sinatra Assessment

- [ x] Use Sinatra to build the app
- [ x] Use ActiveRecord for storing information in a database
- [ x] Include more than one model class (e.g. User, Post, Category)
- [ x] Include at least one has_many relationship on your User model (e.g. User has_many Posts)
- [ x] Include at least one belongs_to relationship on another model (e.g. Post belongs_to User)
- [ x] Include user accounts with unique login attribute (username or email)
- [ x] Ensure that the belongs_to resource has routes for Creating, Reading, Updating and Destroying
- [ x] Ensure that users can't modify content created by other users
- [ x] Include user input validations
- [ x] BONUS - not required - Display validation failures to user with error message (example form URL e.g. /posts/new)
- [ x] Your README.md includes a short description, install instructions, a contributors guide and a link to the license for your code

Confirm
- [ x] You have a large number of small Git commits
- [ x] Your commit messages are meaningful
- [ x] You made the changes in a commit that relate to the commit message
- [ x] You don't include changes in a commit that aren't related to the commit message


Easy enough, right?

![](https://www.meme-arsenal.com/memes/12ffd9d5a40d67af8fa48aa98d476dce.jpg)



**My first step was planning out my app structure using a Model-View-Controller pattern.**

Pro tip: this can be automated by a gem named "corneal" which was built by a fellow flatiron student.

[Click This For Corneal Gem ](https://github.com/thebrianemory/corneal)

![](https://i.imgur.com/XB5Lv2R.png)

# Model
I used two different models: User and Projects. A user class has many projects. A project class belongs to a user.

# View
Typically at the root of the app folder, you'll create two views: index.erb and layout.erb

layout.erb: this file allow common HTML surrounding individual pages (or views) to be shared across all pages. This is where I defined my CSS stylesheet, and HTML <head> and <body> containers.

index.erb: this defines my app’s homepage, showing an image with links for users to sign-up or log-in to the app. 

Both of these files are grouped with two sub-folders, in my case Projects and Users.

**Next up is CRUD** Create - Update - Read - Delete

**CONTROLLER**

I created three controllers: Application_Controller, User_Controller, and Project_Controller.

**Application_Controller:** this controller inherits Sinatra::Base, giving you access to useful methods to define route actions such as GET and HELPERS! This is where you enable sessions and session_secret to encrypt user passwords.

**UserController:** this controller inherits from Application_Controller, and defines RESTful routes relevant to a User

**CourseController:** this controller inherits from Application_Controller, and defines REST route actions relevant to a Course.

# DATABASE
Next, it was time to build out my database!

You can use rake to defined the database tables for each of your model class (Users, Projects).

![](https://i.imgur.com/139EpPW.png)

Dont forget to rake db:migrate

Other helpful commands for when you screw up:

Rake -T

Rake db:reset

Rake db:seed

Deleting system32

ALT + F4

I never raked so much in my life! I spent a lot of time sorting out my migrations and re-sorting my seeded data, etc.


**Here's an idea what your controllers should look like.**

![](https://i.imgur.com/49Pcz0Z.png)

[](https://i.imgur.com/cpIQNaB.png)

What you'll start to notice is that there is a lot of similarities between Sinatra apps. The coding becomes mundane and as lazy coders legend goes, we do whatever we can to be even lazier. Hence Rails was born, which works "magic" and kind of gets rid of the need for us to manually hard-code repetitive and annoying things like this. Cool, right? Right.


You can check out my entire repo on my  [Github](https://github.com/nrozmus/sinatra-final-project)

It was a roller coaster of emotions but in the end, if you truly put your mind to it and keep giving yourself breaks to think about what needs to be done, you will certainly get through it. You're not alone, reach out for help, sometimes "just googling it" is not enough. Utilize your network, whatever it might be.

Thus, in conclusion I'll say:

The record shows,
I took the blows 
And did it my way!

![](https://pbs.twimg.com/profile_images/974682262594666496/ZpteZfMi_400x400.jpg)





