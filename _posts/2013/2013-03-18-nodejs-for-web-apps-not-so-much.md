---
layout: post
title:  Node.js for Web Apps? Not so much.
---

I’m sure I’ll catch some flak for this from the [Node.js](http://nodejs.org/) community (which does seem to be thriving) but I’m just not seeing Node.js as a viable platform for building web applications. When I say web application, I specifically mean websites. The platform seems great for building small servers and daemons and such, but as a complete solution, I’m not seeing it. “Why?”, you ask? Pretty simple reason, and the reason I see cited often times when explaining why Node.js doesn’t do something, it’s that Node.js doesn’t do much for you. That’s great when you need to build a ground up solution that perhaps has never been done before. But for a website? The website workflow already exists and with Node.js you have to start with clean slate.

I can hear the smug “just use [Express](http://expressjs.com/)” comments already. I agree, there are frameworks out there to help alleviate this perceived lack, but I have a huge problem with that, especially with such a new platform (so new there’s not even a major point release yet!). The problem I have is that you end up with a community of users that are reliant on the framework more than anything else. Don’t get me wrong, we see it with other languages too. Job postings looking for Drupal or Django or whatever framework developers, not developers that are strong in the language itself. I do believe that you can be a great framework developer but not overly apt with the language as a whole. This can easily be seen with ORM-reliant developers that can’t write an SQL statement to save their life. Not to mention that the law of the instrument can quickly come into play with developers that are reliant on JavaScript for their entire stack.

The framework-reliance isn’t my only issue at this point, the number of options to solve a single problem was a bit overwhelming, albeit quite impressive considering the age of the platform. With my recent toying around (yes I did toy around with porting a site of mine to Node.js for kicks) I ran into a myriad of [templating options](https://github.com/joyent/node/wiki/modules#wiki-templating), so many that I wasn’t quite sure of which one to go with. Of the engines I researched, they all seemed to have very little traction overall and most of the comparison sites out there only covered a small slice (with not much overlap). The whole thing just feels very fragmented like no one in the community actually talks to eachother before starting a new project (there are quite a few duplicate templating projects out there).

There were a few positives, specifically when it came to workflow. Personally, I always develop locally and fell victim of having to restart the server every time I made a change. `jekyll` has an `--auto` argument to watch for changes, but `node` did not. I did find [`nodemon`](https://github.com/remy/nodemon) which watches for changes and restarts your app when you save your files. The combination of `nodemon` and [`forever`](https://github.com/nodejitsu/forever) clears up some of my early gripes with Node.js but definitely feels a bit more like hackery than anything else.

So that’s where I’m at with it, I won’t be using Node.js for a website in the forseeable future and will most likely go with Python for scenarios where I need to build a small server or daemon (old boring technology is often times very stable and reliable, just saying).