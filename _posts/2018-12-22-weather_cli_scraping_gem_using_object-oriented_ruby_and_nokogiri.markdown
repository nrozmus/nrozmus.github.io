---
layout: post
title:      "Weather CLI scraping gem using Object-Oriented Ruby and Nokogiri"
date:       2018-12-23 01:42:58 +0000
permalink:  weather_cli_scraping_gem_using_object-oriented_ruby_and_nokogiri
---


![](https://linguagloss.com/wp-content/uploads/2016/06/man-confused-at-computer.png)

Yup, it's not easy. In fact I spent most of my time looking like the picture above! I was fustrated, spending hours and hours on the project not knowing where to start. I'll be honest and address the elephant in the room and say you most likely will too. Heck, that's probably one of the reasons you're here!  It's not easy or inherently obvious what you should do and as a beginner, this was terrifying. How was I going to scrape a website with a hierarchial structure for specific data? Well, here's how.. let's get started!



**First step: environment setup**

1. Open your terminal and run ***bundle gem <file_name>*** in your terminal of choice. Remember to CD into your file as well! For some reason I took me a few minutes to figure out. "cd <file_name>". This will give you the basic layout of your program.

Pro tip: Name your gem using underscores, for example "weather_check" is the name of this gem. Using dashes will cause you a lot of pain, we can leave it at that. 

2. Open your bin folder and create a new file named ***<your_program_name>.rb***. Make sure it runs and give it proper command privileges by typing ***chmod +x selection.rb*** into your terminal. Run ***ls-lah*** to confirm that the file has changed. This enables you to run your program like a user would, through the bin/<file_name> command. 

3.  In the lib/*weather_check.rb*, we can address all the different libraries we will need such as **pry, nokogiri and open-uri.**

Install it into your library by running ***gem install <gem_name>*** into your terminal.

![](https://ibb.co/qj7Dfkf)

4. Add your gem dependencies into **weather_check.gemspec.**

![](https://ibb.co/c8rXzCB)


**Second step: Instantiate your classes**

1. Create a file in your lib folder and name it **cli.rb**. This file will be used for your programs interface.

2. Connect it to your **weather_check.rb** file by the "::" syntax. For this example I coded `class WeatherCheck::Weather`. in **cli.rb** I coded `class WeatherCheck::CLI`. 

3. Time to code! The basics are almost always the same for building a scraper. There are a couple different ways of going about it, in this scenario we are not using an `initialize` method. Add your attr_accessor for your values in **weather.rb**. They are `:temperature` and `low`.

4. Configure your classes, methods and variables.  In this program we use the `self` method to grab the object we are creating. Create an empty array, point the data from the scraper to it.

![](https://ibb.co/9wXf2d1)

5. Set up your CLI, you can use fake data to help test your methods as you go about building your gem. Do anything you can to keep moving, attack the project one task at time. One of the last things you want to do is to think about the big picture, instead keep giving yourself small tasks and knock them out one part at a time. You'll move forward faster, and are less likely to get overwhelmed with the task.

![](https://ibb.co/ft6r7gt)

**Third step: Pull out the targeted data**

Great, for some this might be the hardest step. For other's it might be a cakewalk. Keep in mind you want to use a website that is easy to scrape, shoot for one that doesn't have challenging or oddly coded HTML/CSS. Stick away from websites where you would need to implement an API or anything of that sort. Trust me, there's another website out there that's similiar to what you are looking at which will be much easier to scrape.

Anyways, crack open google chrome and inspect your site. Usually right clicking and inspecting will automatically open up the developer tools view and give you the information you need. Be very specific with what you inspect, since it will take you to exactly what you click on and give you the CSS selector that you need to copy.

![](https://ibb.co/9TK4jnz)

For this example I pull out `span.large-temp`. *But wait, there's more!* Each CSS selector will have to be tested and manipulated until it spits out just the right answer you are looking for. In my case `span.large-temp` included not only the current temperature but also the temperature's for the rest of the week! How did I narrow it down to just the first temperature? `.first` will output just the first temperature in this case. Be sure to also add your `text.strip` at the end to clean up how the output looks like.

![](https://ibb.co/KwDJVgz)

Here's how the program operates:

[](https://youtu.be/CMBnJxSiHZg)

**Conclusion**

Work through and plan everything one step at a time. Imagine the code you would want, then do your research and figure out how to make it happen. Listen to your error messages, and really read them. Most of the time they will tell you exactly what's wrong, and it could be something super simple. Anything else that stumps you feel free to google it, part of being in the coding culture is a sense of community, teamwork and being able to utilize your resources. Someone has more than likely encountered your problem before and has solved it, the answer is most likely out there. You're not the first to create the template of a scraper. That's an integral part of how coding and technology is moving so fast. There is no single person who know's all the answers and has all the resources, we have public libraries where we share our work and hope that someone else utilizes it to make something new, hence the MIT license. (permits you to modify others code and create new things)

Finally, I hope I've at least given you insight on how to go about setting up environments, making everything work together and an easy entry point to using nokogiri to scrape websites.

That's it, now get coding!


