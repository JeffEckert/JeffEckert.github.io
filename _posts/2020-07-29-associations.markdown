---
layout: post
title:      "Associations"
date:       2020-07-29 13:21:09 +0000
permalink:  associations
---


So, What is the deal with associations?  Why are they such a powerful thing? Well to get to the answer to that you have to look at the true basis of a website.  

When we look at a Rails app what you are really boiling it down to is a way of connecting different things to make a functional site.  Those things are called Models.  We use these models in conjuctions with controllers to make views that the user can see and interact with.  However to make a truely engaging and natural site you will need these models to interact.  If you are building a site for California Tourism you may have models for your sites users,  tourist locations,  logdging and other things.  But Rarely is a person going to go to a site to access just one of those things.  In order to bring those items together you are going to use associations. Associations can be as broad as things like has many and belongs to right down to something like has many through.  If you look at a has many it is exactly like it sounds, California has many hotels, but each hotel belongs to California.   It gets even more useful to use associations to connect things that may not be directly connected but as a user might need to group them together.  California has many differnt Senic overlooks through state and national park locations. 

In coding this can be extremely useful to help when needing to find particular information or filter information.  The reason for this is when you set up an association you get access to association methods that you can use for those particular associations.  For each association there are numorus methods. The best way to find out what you have access to is to go into your rails console and type your model.method and that will list the different methods you have access to when looking into that model. The amount of methods you will have will change based on how narrow your association is.  Once you have that list of available models you can use that information to access your various attributes for that model and association.  For example if I enter User.methods, I can use User.local_stored_attributes to find out what locally stored attributes I have for User. You could also use your assocations in the method call like StatePark.first.forests.count to get a number of how many state park forests you have connected to California. The helpful thing about this is that you can see as you get more narrowed in your command you get methods that are only for that command.  So if you search User.first.lodgings.methods you would only see methods to help you with your Users have many lodgings association.

This is why associations are so powerful.  They have the ability to allow the developer to be as broad or as narrow as necessary to taylor their project to meet their needs.
