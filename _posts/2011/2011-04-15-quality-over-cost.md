---
layout: post
title:  Quality over cost or how PennySMS sucks and I switched to Twilio
---

For nearly the last two years I’ve run a simple SMS reminder service known as [ReminderWire](http://reminderwire.com/). The site was initially built around the idea of using the built in carrier email addresses for cell phones to send the SMS messages. The major drawback to this was that I had to prompt the users for their carriers and had no way to handle the user changing carriers. After some brain storming about how to make it all work, I discovered [PennySMS.com](http://pennysms.com/). The service was cheaper than most services as there were no up front / recurring costs (oh and 0.01$ per message) and I didn’t have to buy a bulk of credits up front. The service had a simple API and used the same method that I was going to use with sending emails to the carrier email addresses. Best part of it all was the fact that I never received an invoice from them, not that I wasn’t willing to pay for the service, but getting it seemingly for free was pretty bad ass.

Fast forward to a more recent time. Overall PennySMS has been only semi-reliable with frequent issues of being unable to send messages. The API still being accessible, but returning nothing but errors. Then one day [Recess Mobile](http://recessmobile.com/) announces they are buying the service, touting a more reliable service and upwards of 6 years of previous experience in the industry! First order of business, they finally got me an invoice and the service had been a bit more reliable than in recent months.

Fast forward to the last couple of months, the service has been flaky at best and within the last week or so Recess Mobile has contacted me to advise that they are going to shutting down PennySMS and replacing it with a new service. This new service is again touted as reliable, but wait, you already proved you couldn’t do that guys. The new pricing to be a part of the Beta for [“Carousel” SMS Solution](http://transactionalsms.com/) is 25$ per month in addition to a 0.01$ per message pricing. The positive is that the new service is going to be “real SMS” and not the hacky email solution. Sadly at this point, the pricing seemed better than needing to go back and explore services with pre-paid “credit” systems or buying a GSM modem and attempting to roll my own solution.

Insert [Twilio](http://twilio.com/), recommended to me as an amazing mobile platform with great pricing structures. Signing up for an account, I knew these guys were legit. A dashboard with usage metrics and errors and all that shit you’d expect from a paid service. But what’s it cost? Pretty simple pricing, you pay per line and you pay per usage. A local line (since you can’t do SMS over a toll-free number) is a mere 1$ per month, and usage is 0.02$ per message. Did I mention a 30$ credit for signing up? I made the mistake of using 2 bucks of that to reserve a toll-free number that I couldn’t send SMS from (my bad) but overall everything has been great. ReminderWire is up and running and I’m actually feeling confident about it’s stability.

So that’s the story of how I ended up paying more than twice as much per month (1 penny versus 1 pennies + 1$) to support ReminderWire. You forget sometimes that it’s actually worth it to pay more for something that actually functions (quality over cost) and lucky for me Twilio came about!

On a side note, it took only about 15 minutes to swap out PennySMS for Twilio’s API… amazingly simple with the pre-built libraries provided (results may vary).