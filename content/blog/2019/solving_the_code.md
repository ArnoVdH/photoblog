+++
title =  "Solving the Code"
date = 2019-09-07T10:00:00+02:00
categories = ["intro", "hugo"]
featured_image = ""
description = ""
draft = false
+++

Since I'm a complete and utter novice at all... *this*, there were quite a few difficulties in getting this blog up and running. In this post I'm trying to describe how (and why) I built the site this way, talk about some of the obstacles I encountered and how I solved them.

<!--more-->

Folder structure
----------------

    .
    ├── archetypes/
    │   ├── blog.md
    │   ├── default.md
    │   └── photo.md
    ├── content/
    │   ├── blog/
    │   ├── photo/
    │   ├── _index.md
    │   └── about.md
    ├── data/
    ├── layouts/
    │   ├── _default/
    |   |   ├── baseof.html
    |   |   ├── list.html
    |   |   └── single.html
    │   ├── blog/
    |   |   ├── list.html
    |   |   └── single.html
    │   ├── categories/
    |   |   └── list.html
    │   ├── partials/
    |   |   ├── blog-nav.html
    |   |   ├── footer.html
    |   |   ├── head.html
    |   |   ├── header.html
    |   |   ├── pagination.html
    |   |   └── photo-nav.html
    │   ├── static/
    |   |   └── single.html
    │   └── 404.html
    ├── static
    │   ├── css/
    |   |   └── style.css
    │   └── img/
    ├── themes/
    └── config.toml

Layouts pages
-------------
I decided not to use a homepage.html layout, and to use a normal photo-centric list-page as my homepage. This way I could make my homepage and my photopage to be one and the same, which was my intention after all. The blog side of the site would be different, so I made a seperate list.html for the blog section. I'm sure there are other ways of doing this, but this seemed to work and served my purposes.

Main menu
---------
At first I just built a menu in my header with html. That was before I discovered the menu template options in Hugo. With some tweaking of the original html, I could have active menu options to make navigating the site somewhat easier. The problem was that the menu link to the 'About' page didn't register as active. In the end, I used a slightly less satisfying but working fix by putting `menu = "main"` in the about-page frontmatter (and removing the duplicate from the config). The individual pages don't show the active sections of the site, but that's something to fix later.

Navigation menus
----------------
Since this site has two parts, I wanted a distinct navigation menu for each one of those parts. So you can navigate both the photography portfolio and the blog in it's own way. I made seperate `nav` partials for this purpose. The photo-nav one ranges over the photo series and it's tags, the blog one ranges over the categories (which I use as the blog-side variation on tags). 

Pagination
----------
Of course I needed a way to show my posts over multiple pages. I'd love to have a infinite scroll type blog one day, but a basic page system seemed an easier and more stable option.

I had quite some difficulty wrapping my head around the code, so in the end I took the liberty to "borrow" some code from [here](https://glennmccomb.com/articles/how-to-build-custom-hugo-pagination/) and added it in as a pagination.html partial to be added to the templates where needed. 

CSS: Grid
---------
Haven gotten everything to work is one thing (and I was already kinda jubulant about it at this point - I mean, it *worked*!), but now everything was just a vertical mess. All the menu's, content, pagination buttons, etc. were one after the other.

I knew that the whole CSS portion of it all would take up *at least* as much time, if not more, to get it right, with all the tweaking and finetuning, testing and rebuilding that would come. And I was kind of scared of how to do it all with those flexboxes I'd been reading about.

But then I read about CSS: Grid and it looked like a great way to built a standard layout the easy way. It turns out it's *easier* maybe, but not easy. But with a few lines of codes I made a responsive website. And apparently it's necessary to put those media queries at the end of your css to make them work.

Responsive images
-----------------
Since one of the main goals of this website was to present my photographs in a clean way on the main page, I had to figure this one out properly. I learned that just adding the images (even in a web optimized way) doesn't cut it, since they tend to ruin the page layout without the ability to adapt for diffferent screens. I wasn't even thinking about presenting on mobile yet! In other words, I needed them to be *responsive*.

Helpful resources
-----------------
From which I shamelessly stole, copied and adapted code.
* [The Hugo Documentation site](https://gohugo.io/documentation/)
* [The Introduction to Hugo Youtube series by Mike Dane](https://www.youtube.com/playlist?list=PLLAZ4kZ9dFpOnyRlyS-liKL5ReHDcj4G3)
* [This blog by Zwbetz](https://zwbetz.com/make-a-hugo-blog-from-scratch/)

Closing remarks
---------------
I'm very much aware that many of my 'solutions' are very crude or inelegant. But this was and still is my own little learning project. I've had a lot of fun trying to figure out solutions for all the problems that inevitabely kept creeping up on me. 