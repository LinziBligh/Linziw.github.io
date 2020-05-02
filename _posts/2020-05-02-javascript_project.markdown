---
layout: post
title:      "Javascript Project"
date:       2020-05-02 10:11:55 +0000
permalink:  javascript_project
---


The requirements of the projevct were to create a SPA - Single Page Application with an HTML, CSS, and JavaScript frontend and a Rails API backend. Also all of the interactions between the client and the server must be handled asynchronously (AJAX) and use JSON as the communication format. The model served by the Rails backend must also include a has-many relationship, and use at theast 3 AJAX calls to cover at least 2 of the CRUD methods, using restful conventions  The project must use classes (Object Oriented JavaScript) in order to encapsulate related data and behavior.

As we were in lockdown in our house during the Covid-19 epidemic, and struggling to get a food delivery slot for our family, I decided to make an application that would help people to at least share their slots with other people in order to use the full capicity of their delivery and increase efficiency.  

Using Javascript to make a SPA was very difficult and repetitive, and didnt seem like the best tool for the job, I feel like Rails and not an SPA would have made it mush easier. I had to place all the elements that I wanted on the HTML layout, but hide and reveal sections of the page as we moved through the application. Im not sure if that was the best way of doing it, but it cetrainly made it very challenging, and made for many lines of code before I refactored. I discovered a toggle method that was useful for remove the "hidden" class and putting it back when I needed it, so i just made a sequence to be run between pages to get the view I wanted.

The has-many relationship that I used was one user "has many trolleys" which I think satified the requirements. The ajax calls that I used were

Post request to Users to create new user
Post request to Sessions to login
Get request for all trolleys in the future,
Post request to add a new trolley
Request to Postcodes.io to verify postcode and get longitude and latitude data
Get request to delete trolley
Post request to edit trolley

Perhaps the hardest element was to figure out how to sort by distance, which meant taking the postcode and sending a request to postcode.io api to get back longitude and latitude data, then using a "get" function in my trolley class which compares each trolleys location with that of the user that is logged in (Haversine Formula), then sorting those results in order. I found this by using google, I never would have figured it out by myself!

```
function getDistanceFromLatLonInKm(lat1,lon1,lat2,lon2) {
  var R = 6371; // Radius of the earth in km
  var dLat = deg2rad(lat2-lat1);  // deg2rad below
  var dLon = deg2rad(lon2-lon1); 
  var a = 
    Math.sin(dLat/2) * Math.sin(dLat/2) +
    Math.cos(deg2rad(lat1)) * Math.cos(deg2rad(lat2)) * 
    Math.sin(dLon/2) * Math.sin(dLon/2)
    ; 
  var c = 2 * Math.atan2(Math.sqrt(a), Math.sqrt(1-a)); 
  var d = R * c; // Distance in km
  return d;
}

function deg2rad(deg) {
  return deg * (Math.PI/180)
}
```

I also used a css template for my styling but ended up editing it a lot to fit my needs, and it ended up taking me hours to make it work as I needed it.

This was by far the biggest challenge as has taken me nearly three full weeks for what appears to be a very simple app! I didnt bother adding in any support for the transaction between people other than a template email, but hope to eventually add a feature that reduce the amount of spaces left in someones trolley as people approve requests from others.


