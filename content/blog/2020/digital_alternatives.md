+++
title =  "Digital Alternatives"
date = 2020-07-12T21:03:00+02:00
categories = ["Personal", "Internet", "Project"]
featured_image = "/img/matrixcode.jpg"
description = "A post about my efforts to get away from the big data corps"
draft = false
lastmod = 2020-07-27T22:15:00Z

+++
This blogpost is a list about my search for digital alternatives that are more open, more respectful and more private than the ones I and a lot of other people have been using until now, often for free. It's an attempt to claim back ownership of my virtual self. 

Why did I do this? These last few years I've started to shift away from trusting the big data corporations such as Google and Facebook. I'm suspicious about the free services these companies offer us. Not only are they invasive of our privacy, they also profit of the enormous amount of data that we generate for them. This way these companies have a huge impact on our consumption, on our ideas, on our relations, on our society and democracy. They are also not held accountable for anything and sooner or later the repercussions will catch up with us - if they haven't already.

<!--more-->

I decided somewhere last year that I needed to change my own internet habits and the services that enable them. While my shift towards suspicions was quite sudden, it also dawned on me that actually stepping away from it all would be hard. Not just because it's difficult to find alternatives - it is a little, but sites like [AlternativeTo](https://alternativeto.net/) give lots of crowd-sourced options - but more importantly because they are imbedded in your social life too: people share the same social networks, use overlapping services that have great integration (collaborative working with Google Docs for instance), or account-managing through other social media (logging in with your Facebook or Google account). Of course it's always possible to find alternatives of step away from these corporations entirely - well, not *really* entirely since they also keep track of non-users with shadow accounts - but once you're a user that's been pulled into the ecosystem of Big Tech, you're bound to lose something when quitting.

So this is more than just a list of choices, this is also the still unfinished journey to save myself, and reclaim ownership, as data-set. This website is part of that, as an outlet for what I do. But there is so much more to do. So I tried to break this journey up into different parts. Some of them are done, some of them are a work in progress, some of them have been thought about but not yet implemented and others are just very difficult to find satisfactory solutions for.

I also know that I'm far from perfect. There will be people who'll have issues with some of my choices, think they know it all better (and they probably do). I am not a high-tech wizzkid that's capable of doing everything himself, nor am I a privacy saint or a recluse who's prepared to give it all up in the name of security.

A quick word on self-hosting: in quite a few of the cases below, self-hosting would be a great option, especially if you're tech-savvy enough and have a higher risk profile. I'm neither, so I chose other options.

## E-mail
**Status: done ✔**

This was actually pretty easy to do. One of the reasons, I guess, is that, for one thing, e-mail has a long established history pre-dating the contemporary internet giants. There are quite a few privacy oriented possibilities available.

I opted to use [posteo](https://posteo.de/en), a German e-mail provider with quite a comprehensive privacy policy and transparent communication and a very fair pricing policy (1 euro per month). I think that paying for such a service is worth it; this way I don't get served advertisements and the provider will have less incentive to sell-out and compromise my data. Posteo uses green energy to run their services and offer multiple security measures such as encryption, 2FA (two-factor authentication) and anonymous payment options.

## Security
**Status: done ✔**

I really needed to start using unique and more difficult passwords for all my accounts, so that one leak wouldn't compromise everything. For years I had the bad habit of using only a limited set of (far too easy) passwords. Switching to another e-mail provider proved to be the ideal reason to start using a [password manager](https://en.wikipedia.org/wiki/Password_manager) for added security and easy account management. I myself use [Bitwarden](https://bitwarden.com/). It's open-source and has encrypted cloud storage of your password vault so I can access it on multiple devices easily.

## Calendar
**Status: done ✔**

The actual calendar was easy: it came with a posteo account (together with an adress book). Easy enough to use on my desktop. The problem was setting it up to sync with an app on my smartphone, so I could use it as my planner. This required quite a bit of trial and error and fiddling. In the end I used aCalendar+ as the calendar app itself and DAVx<sup>5</sup>, a payed app, to make synching with CalDAV possible. I've been using it for more than a year now and I'm very happy with it. The only issue that I encountered were some birthdays that had their month and day switched, which led to some akward conversations, but all took it in good humour.

## Chat & messaging
**Status: done ✔**

More than a year ago I did some research into this and I decided to stop using WhatsApp and Facebook Messenger on my smartphone and switch to [Signal](https://signal.org/) completely. Signal *isn't* the most secure messaging app out there, but it's very accessible. It's run by a non-profit organisation and it's software is completely open-source and the encryption protocol they developed is also used by WhatsApp.

I sent a message to friend and family that I would stop using WhatsApp and that they could reach me through Signal (with a little explanation urging them to do the same) or through regular text messages (sms). My core group of friends followed, my family didn't. So be it.

## Search page
**Status: done ✔**

There are multiple alternative search engines to replace the omnipresent Google. For a time I used Searchpage, but they have been since bought by an advertising company so I decided to switch over again. Some other alternatives I considered where Ecosia (focus on ecology by planting trees with revenue), DuckDuckGo (focus on privacy but based in the US), Searx (open-source, privacy-oriented, federated and meta-search) and Qwant (EU based, focus on privacy, proprietary software but developed in collaboration with the French government among others). For now, I've been using Qwant and I'm quite happy with the results.

## News & Feed
**Status: to do ✘**

One of the things I use Facebook for, just like many other people on our planet these days, is as a source of news. This is problematic to say the least, but they *are* pretty good at giving you a good overview without overwhelming the user. This was a huge problem when I tried to switch to using a regular RSS feed: as soon as I started following two or three news-sources, I quickly became overwhelmed by updates and notifications. This seemed counterproductive. So I started looking for a feed aggregator that has some way of filtering or an algorithm that keeps it accessible to me.

## Social networking
**Status: to do ✘**

I honestly think this will be the most difficult part of the transitioning, since this isn't just a technical problem to be overcome, but more importantly a social one. Due to the network effect, switching to another network means a huge loss. Unfortunately most commercial social networks don't communicate between eachother, let alone federate.

There are some alternative social networks, mostly federated and built around technology like ActivityPub. There's Mastodon (a Twitter clone), Diaspora (a Facebook like social network) and some more. But most of these are very niche.

Another possibility would be to make a social network between websites themselves. This could be done through some sort of advanced RSS or the Webmention technology.

## Maps & route planning
**Status: to do ✘**

There aren't really that many alternatives to Google Maps, since making a (world)map isn't very easy. The most well-known is OpenStreetMap, a collaborative, open-source effort that works pretty well... Except for public transport help it seems. Which is unfortunate since I do rely on it quite a bit.

## Cloud storage
**Status: done ✔**

I wanted a service that worked well on multiple platforms (Windows, Linux, Android), offered a decent amount of free storage space and had reasonable pricing for future use. Respect for privacy was also important. I ended up using [pCloud](https://www.pcloud.com/eu) for this.

## Desktop operating system
**Status: done ✔**

I made the switch to Linux during the summer. One of the big issues, as with anyone wanting to switch, is choosing which distro to use. After some deliberation and research I decided to go with [Manjaro](https://manjaro.org/). Not only was it recommended to me by a friend, it's also accessible yet cutting-edge enough for my needs, since it's based on Arch Linux. It's also an experiment in gaming for me, using [Proton](https://github.com/ValveSoftware/Proton).

## Mobile operating System
**Status: to do ✘**

This is something I would want to do in the future, but is big hurdle since the Android platform is more tightly integrated and would require more work to be able to do all the things I expect of a smartphone. The main possible OS replacement for Android seems to be [LineageOS](https://lineageos.org/) right now. Instead of using the Google Play Store to install apps, there's the F-droid store with open-source alternatives.