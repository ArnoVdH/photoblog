+++
title =  "Solving the Code"
date = 2019-07-15T19:54:25+02:00
categories = ["intro", "hugo"]
featured_image = ""
description = ""
draft = true
+++

Since I'm a complete and utter novice at all... *this*, there were quite a few difficulties in getting this blog up and running. In this post I'm trying to describe how (and why) I built the site this way, talk about some of the obstacles I encountered and how I solved them.

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
Why no homepage.html file.

Navigation menus
----------------
Since this site has two parts, I wanted a distinct navigation menu for each one of those parts. So you can navigate both the photography portfolio and the blog in it's own way. I made seperate `nav` partials for this purpose.

Pagination
----------

CSS: Grid
---------
Haven gotten everything to work is one thing (and I was already kinde jubulant about it at this point - I mean, it *worked*!), but now everything was just a vertical mess. All the menu's, content, pagination buttons, etc. were one after the other.
I knew that the whole CSS portion of it all would take up *at least* as much time, if not more, to get it right, with all the tweaking and finetuning, testing and rebuilding that would come. And I was kind of scared of how to do it all with those flexboxes I'd been reading about.
But then I read about CSS: Grid and it looked like a great way to built a standard layout the easy way. It turns out it's *easier* maybe, but not easy.

Responsive images
-----------------
Since one of the main goals of this website was to present my photographs in a clean way on the main page, I had to figure this one out properly. I learned that just adding the images (even in a web optimized way) doesn't cut it, since they tend to ruin the page layout without the ability to adapt for diffferent screens. I wasn't even thinking about presenting on mobile yet! In other words, I needed them to be *responsive*.

Helpful resources
-----------------
From which I shamelessly stole, copied and adapted code.

Closing remarks
---------------
I'm very much aware that many of my 'solutions' are very crude or inelegant. But this was and still is my own little learning project. I've had a lot of fun trying to figure out solutions for all the problems that inevitabely kept creeping up on me. 