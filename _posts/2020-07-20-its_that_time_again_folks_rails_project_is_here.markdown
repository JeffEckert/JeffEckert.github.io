---
layout: post
title:      "Its that time again Folks!! Rails Project is Here!"
date:       2020-07-20 12:43:43 +0000
permalink:  its_that_time_again_folks_rails_project_is_here
---


For this project I wanted to stay in the same vein as my Sinatra project with Disney Vacations.  However instead of having an app that can allow you to take notes about your favorite attractions, This app would allow you to choose attractions and organize them into a vacation plan.  The site is called the Disney Vacation Planner.  

The first thing I had to do was formulate a plan,  so I went to the trusty draw.io page to try to roughly lay out my models and how they were going to connect. I knew I needed to have a user that would log in so I started with that.  I also needed some has many and belongs to relationships.  In this project I also was required to have a nested route,  so from there I started thinking about the flow the user was going to have.  The user needed to be able to see the attractions,  then group them into something I called a vacation plan.  What I decided to do was to make the way the user could group the attractions with their vacation plans.  So I created a join database I called a highlight.  This would allow the user to select an attraction but then also to add info to it like the day they wanted to go to it and any notes, then once they had that they added it to their vacation plan.  So this meant that Vacation Plans Had many Highlights and also had many attractions.  Because the users didnt need to access highlights accept to add them to a vacation plan we nested that route through vacation plans.  

Another new feature that I was able to add to my site for the first time was OmniAuth.  This allowed me to add a feature for the users which allowed them to use their github accounts.  This was helpful to the site for two reasons,  1.  It gave the user more options to log in and 2.  It allows authentication to be done through github for those users so the site wouldnt have to be responsible.  When a user logs into our site using github they are transfered to a github site where they are verified, that verification gets sent to our site and added to our users Database and that user is allowed to log in as a normal user.  

All in all I feel my rails project was very successful many new things were added since rails and the site looks much more verbose.
