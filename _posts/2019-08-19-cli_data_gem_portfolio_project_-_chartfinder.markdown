---
layout: post
title:      "CLI Data Gem Portfolio Project - ChartFinder"
date:       2019-08-19 19:52:26 +0000
permalink:  cli_data_gem_portfolio_project_-_chartfinder
---


So, the original idea for this gem came about after a discussion with my colleagues at work about what was number 1 in the music charts on the day we were born, and whether or not that "says anything" about that person! 

After initially finding it tricky to quickly look this up using Google, I thought it would a good idea to do this as a simple project. In order to stick to the requirement of doing something that initially "brings up a list" then bring up more information on an item in that list by going "one level deeper", after a discussion, the concept was changed slightly to simplify it to initially bring up the whole music chart for the date entered.

After initially looking at scraping Wikipedia, it turned out, the Official Chart Company's website was much easier to scrape as you could simply change the date at the end of the url to bring up the page with the chart on that I was looking for. This was very handy except that I had to make a method to reformat the date entered and swap it about to fit the same pattern, which took me a while. (YYYYMMDD).

In my early commits, I got the gem working perfectly by just scraping the attributes of Title, Artist, Record Label and Coverart link, saving them into a hash for each song, then pushing that hash into an array. I then iterated through that array in my CLI class to display the date.

I felt that this might not fulfill the requirements of being Object Oriented enough, so I then split up my song class to create  seperate scraper and song classes that had their own responsibilities, scraper to get the information, and song to create song objects from that data. I then used these song objects in the cli class to display the information.

Im so proud of this first project, its the first bit of solo coding I've ever done!

At some point I hope to update it with a "soundtrack to your life" feature, where it will bring up the number one on your birthday for every year of your life in a list, which maybe you could then export to a Spotify Playlist or something similar!
