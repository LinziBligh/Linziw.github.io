---
layout: post
title:      "TribeRide - Rails Portfolio project"
date:       2020-03-13 14:23:32 +0000
permalink:  triberide_-_rails_portfolio_project
---


So, I really struggled to come up with a theme for a project, until I stumbled across a real world issue that needed solving.

As a user of a Peloton bike (well not the actual bike, too expensive, but a generic bike and an ipad app) and a corresponding Facebook group (UK Ladies Peloton), we like to organise rides in a weekly schedule so that  instead of riding alone, at home,  you can be part of a tribe that all ride together at pre-arranged times.  This means you can see each other on the leaderboard and "Hi Five!" each other for encouragement, whilst at the same time to feel like you’re riding together with names you recognise.

The current method is a Facebook post listing all of the upcoming rides for this week, so I thought i'd make an app that allowed the owners of the Tribes to publish the weekly rides, Users to join individual rides and see who else is participating, and join multiple tribes if they want to.

I really found it helpful to plan out user stories and diagram a schema, I soon found that it would be a lot more complicated than I first thought, and I got myself in a bit of a muddle at first with admins and owners etc. I created a skeleton app on github to test all of the associations but there still a few that i missed along the way!

First I generated the basic resources that I needed to set up my app, and then migrated each one at a time to check the schema was correct. Having 5 models for this application took a bit of trial and error in terms of the associations, so I had to play about with it in rails c first before i started building the routes and views.

Whilst building, I inspected params constantly to figure out what was going on with my forms, and i used binding.pry to debug as I went along. I struggled hugely with the styling, at first attempted to use a bootstrap theme, but I couldnt get it working properly, so I just borrowed the elements of the theme such as the cards, and got rid of everything else as it was very over complicated. I think the styling definately needs a lot of improving, and im finding its the thing I enjoy the least, but unfortunaley seems to have to most impact!

I very much enjoyed this project, and once I got going, I found I worked quite methodically, creating a route and checking it worked first before linking it up to a sample view file, then trying to get some data from the models into the view, and adding the buttons etc. I feel a lot more confident about approaching a big project now.

I've learnt so much on this project, and I really feel its consolidated the Rails chapter well, but I very eager to move onto the Javascript section now!
