---
layout: post
title:      "Chartfinder - React Edition - Building my final portfolio project."
date:       2020-09-07 13:15:26 +0000
permalink:  chartfinder_-_react_edition_-_building_my_final_portfolio_project
---




So here it is, possibly my final blog post as part of the course! Throughout my course I wanted to update my original CLI Gem scraper project and I thought what better opportunity to show my progression than to turn that original project into a React Web app!

It was much harder than I realised, not least because of Covid-19 rendering my childcare useless and cutting my projects working time down to the duration of Finding Nemo or Frozen each day.. However I kept notes along the way so I could write up a blog post on how I achieved something I’m very proud of in difficult circumstances.

The first thing I found tricky was actively switching between coding in Ruby for the back end and javascript for the front end. It was a good test of my Ruby skills from long ago to see how much I could recall, which as it happened, wasn’t a lot! I had to look up everything in my notes or on forums every step of the way during this build, but I think that’s okay! 

I had to figure out how to start my API on a different server so that I could work on the front end at the same time, and eventually figured out I could do this by starting rails using “rails s -p 3001” instead.

So because I rebuilt my original scraper app, I re-used a bit of my old nokogiri code from my first project to help me build my scraper. Turns out I had to add a lot of logic to it, in order to check for existing instances of the chart in my database first before scraping.

Unfortunately no api exists for the Official Uk Chart, so I still had to continue using my scraper, but eventually I hope to scrape all of the information needed and store it locally in a database to speed things up, and to annoy the official site less with requests!

One of the trickiest things to implement was how to organise each chart, in that you look up a specific date, but each chart is valid for a whole week until its updated the following week. So each chart is good for a week, however over the years, the day they update the chart differs, so I literally had to scrape the start and end date for each chart, then save those to search in between when looking up which chart to retrieve.

I used a ruby gem called “r-spotify” in order to facilitate searching for a spotify id for each track in order to use that to grab the artwork and create the iframe for each song preview.

Another issue that I had to figure out which I don’t believe we were taught during the course was how to stop redux from resetting every time you refresh the page. After much trial and error and reading blogs, I read that you can save a copy of the current state to the browser’s local storage after each action, and when you refresh you can check that local storage first before loading the default state, which means the user can stay logged in and everything stays on the page where it should be.

All in all, I honestly found this project very difficult, but it works and i’ve learned so much in the process of making it, that it was still very enjoyable to make. I loved researched how to interact with Spotify and exploring how to use other people’s gems in my project.

