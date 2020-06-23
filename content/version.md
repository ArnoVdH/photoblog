+++
date = 2019-07-10T08:00:00Z
description = ""
featured_image = ""
tags = []
title = "Version history"
type = "static"

+++
Overview of to-do's, ideas for, and (major) changes to the website.

### To do
* Make images more responsive and lighter (and add lazy loading?)
* Built shortcode to insert images in photo page from a folder
* Implement page bundles
* Adapt header menu to fully use hugo code (make single pages and subpages active)
* Clean up CSS
* Add a graphic logo
* List the 'series' chronologically in nav-menu
* Make page title reference the site as a whole
* Add favicon
* Add info (metadata) about the pictures that show up only when activated
* Add certain (static) pages to (dropdown?) menu under About

### Ideas
* Implement social networking protocol (Webmention?)

***
### 0.9.10 (2020-06-23)
* Changed baseURL to https://arnovdh.be/ to keep the blog's URL constant
* Added shortcodes folder
* Made a photopost.html shortcode to range over images in page bundles to make photoposts easier. 
* Set all old photoposts to draft=true and built bundles for all of them 

### 0.9.9 (2020-06-17)
* Added a render hook to make images lazy-loading. Code taken from [here](https://nickmchardy.com/2020/05/adding-lazy-loading-for-images-in-hugo-static-site-generator.html)
* added a _markup folder

### 0.9.8 (2020-04-25)
* Changed link page name to ':filename' instead of ':slug' for better URL management.
* Removed ':month' from permalink configuration

### 0.9.7 (2020-04-24)
* Changed baseURL to https://arno.netlify.app/ after Netlify decided to migrate
* Added about-menu data to certain static pages in anticipation of implementation of drop-down About menu

### 0.9.6 (2020-04-13)

* Changes to blogpost images css
* Started adding featured images to relevant blogposts & for all photo posts

### 0.9.5 (2020-04-12)

* Changed footer to copy-left

### 0.9.4 (2019-12-05)

* Bought and linked domain name (https://arnovdh.be/)
* Added movie list static page

### 0.9.3 (2019-09-22)

* Added games static page
* Renamed curriculum to timeline

### 0.9.2 (2019-09-15)

* Reorganized responsive css layout for mobile devices (changed order in css file)
* Fixed margins
* Added a curriculum (life overview) page

### 0.9.1 (2019-09-11)

* Reworked the `photo-nav` and `blog-nav` partials to sort tags and categories by count and limit them to most used ones
* Fixed categories list page to show only the summary instead of the complete text
* Added a book list page

### 0.9 (2019-09-09)

* Draft version hosted on Netlify (https://arno.netlify.com/)
* Started the ubi-introduction blogpost
* Lots of tweaks to the css
* Added this version history static page

### Earlier versions

Read [this blogpost]({{< ref "/blog/2019/building_a_website.md" >}}) on how I started building this website.

* Built a basic website with hugo, html & css
* One part is the photography portfolio
* One part is personal blog
* Wrote a few introductory blogposts about building this website
* Saved in a repository on GitHub and linked a Netlify website to it for hosting purposes