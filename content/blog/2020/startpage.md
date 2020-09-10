+++
title =  "Startpage"
date = 2020-09-10T21:05:00+02:00
categories = ["project", "internet"]
featured_image = "/img/startpage.png"
description = "About my personal startpage"
draft = false
lastmod = ""
+++
A little side project I'm working on is building a simple, cohesive start page to use as starting point for the internet, with a built-in news-feed. One of the reasons is that I still want to break free from the corporate algorithms deciding what I see online and thus influence how and what I'll discover and visit.

It's not that big of an idea and there's a small scene online of people designing these, inspiring me to do the same. It will involve mainly some webdesign in HTML and CSS, which I understand a little by now, and probably some JavaScript, which I don't know at all.
<!--more-->

Some of the goals I have for the startpage:

* Sober layout. I like the 'terminal' style because it also communicates the self-reliance idea into your browser. And it looks cool, damn it!
* A comprehensive collection of my most used sites for easy access
* A functional search bar, preferably with some sort of autocomplete function
* An RSS reader: a portion of the screen that show me the top 10 stories or something. Implementation of the reader is more important right now than getting a useable feed, that would be done externally anyway.
* Hosted on github and synched on my cloud drive so I can use it on all my devices.

{{< figure src="/img/startpage.png" caption="What it looks like">}}

### Bookmarks
These are just some links to my most used sites, grouped in categories: social networking, media, personal, miscelaneous... This is just written out in plain HTML. It's easy enough to change categories and swap sites. By using my startpage to group my most used sites I can leave the bookmark-bar away. This way I can free up some extra screen real-estate (most importantly on my small notebook) and I'm somewhat less tempted to just randomly open a new tab to whichever social media site and get drawn into the attention-hoover.

### Search bar
The searchbar works and can be set to use whatever search engine you'd like to use (in my case it's Qwant). It lacks the autocomplete function unfortunately, which makes it less useful than the normal adress-bar-search built into the browser.

### RSS-feed
This was one of the more important things for me and I'm happy I got it working (with the help of reddit user [StringOfRandomInput](https://www.reddit.com/user/StringOfRandomInput)). There's an javescript program running behind this all - that I don't really understand to be honest - but there's also some more comprehendible and editable script where you can input a link to an RSS-feed and then gets limited to the last x amount of posts that get shown in a right pane.

### CSS
The terminal-like style and layout has been adapted from what I found in the [r/startpages](https://www.reddit.com/r/startpages/) community and [this guide](https://stpg.tk/guides/).