+++
date = 2019-07-10T08:00:00Z
description = "Version history of this blog"
featured_image = ""
tags = []
title = "Version history"
type = "static"

+++
Overview of to-do's, ideas for, and (major) changes to the website.

### To do & ideas
* List the 'series' chronologically in nav-menu
* Add info (metadata) about the pictures that show up only when activated
* Implement social networking protocol (Webmention?)
* Change how layout works
* Restyle menu & add logotype
* Fix featured image in page bundles
* Implement responsive images
* Fixes for mobile view

***

### 1.0.1 (2020-07-12)
* Because of some wonky mergers done through another computer I lost most of my work since june. I had to revert and restore an older version. It's possible that some older issues were 'restored' with it.

### 1.0 (2020-06-26)
* Added RSS feed functionality
* Added CSS style for inline images
* Restyled header CSS for mobile use; at least it's functional
* Reorganized the static/img folder and matching links

### 0.9.12 (2020-06-25)
* Rewrote the CSS stylesheet from scratch (unfortunately this did *not* make it easier to fix my original problem)
* Switched to using the 'figure' shortcode from hugo for images (and associated captions) in blogposts
* Moved the logotype AVdH outside of the `<header>` scope

### 0.9.11 (2020-06-24)
* Added favicon to head.html partial
* Added nested list in header.html for dropdown menu
* Added css to make dropdown menu (semi)functional

### 0.9.10 (2020-06-23)
* Changed baseURL to https://arnovdh.be/ to keep the blog's URL constant
* Added shortcodes folder
* Made a photopost.html shortcode to range over images in page bundles to make photoposts easier. 
* Built page-bundles to render the photoblog, using the shortcode mentioned above.
* Removed all single photoblog pages
* Compressed all photoblog images an additional ±45% in size

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

* Changes to blogpost images CSS
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

* Reorganized responsive CSS layout for mobile devices (changed order in CSS file)
* Fixed margins
* Added a curriculum (life overview) page

### 0.9.1 (2019-09-11)

* Reworked the `photo-nav` and `blog-nav` partials to sort tags and categories by count and limit them to most used ones
* Fixed categories list page to show only the summary instead of the complete text
* Added a book list page

### 0.9 (2019-09-09)

* Draft version hosted on Netlify (https://arno.netlify.com/)
* Started the ubi-introduction blogpost
* Lots of tweaks to the CSS
* Added this version history static page

### Earlier versions

Read [this blogpost]({{< ref "/blog/2019/building_a_website.md" >}}) on how I started building this website.

* Built a basic website with hugo, html & css
* One part is the photography portfolio
* One part is personal blog
* Wrote a few introductory blogposts about building this website
* Saved in a repository on GitHub and linked a Netlify website to it for hosting purposes