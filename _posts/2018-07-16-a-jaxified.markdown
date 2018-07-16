---
layout: post
title:      "A-JAXIFIED "
date:       2018-07-16 15:41:57 +0000
permalink:  a-jaxified
---

When I read Jesse James Garrett's "Ajax: A New Approach to Web Applications", it blew me away how much Ajax was resonsible for a revolution in technology, and how I barley remember a world without it. From Google to Uber, almost every technical interface I engage with on a daily basis relies on the power behind this paradigm of multiple technologies working together. 

It also amazed me how much of a learning curve Javascript and ajax took me on coming from Ruby. Although I didn't enjoy coding Javascript or front-end at first, I'm beginning to embrace the power behind this asyncronous language. And, I realize, trying to fight off the reality that most web-based applications today are running on ajax and jquery isn't a far cry from delusion. 

The biggest challenge I faced when adding my jquery front-end to my rails application was a bit of an xy problem. I incorporated a show page for a User's Bookings' instances with a 'Next' button to view all their bookings using an ajax get request to fetch the next booking's information. The problem came from not realizing that I need to wear two different hats when in Ruby and Javascript worlds. I was attempting to update the new booking's links on the DOM by grabbing the link on the page and dynamically interpolating the next booking's route. I had hard-coded the edit link using erb tags in Ruby on the show layout and wasn't realizing I needed to add the associated 'Edit' links through jquery after the individual booking page was loaded. I tried every way I could to grab that link and dynamically change its route, but until I took off my Ruby hat and had awareness of my surroundings, I wouldn't ever be able to see the real problem. 

I'm excited that this is the beginning of truly coding full-stack applications. Although I'm just scratching the tip of the tip of the iceberg- I still have a 360-degree view of all the components to create a synergistic, working application- from domain to DOM. 

