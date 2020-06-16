+++
title =  "The code revisited"
date = 2020-06-15T10:44:34+02:00
categories = ["hugo"]
featured_image = ""
description = ""
draft = true
+++

I've built this website almost a year ago during the summer days. This year, the summer arrived two months earlier than it is supposed to and this takes me back mentally to those days. Maybe that's why I've been looking into the behind-the-screens mess that is this blog. First lesson learned: letting things lie for long times will make it more difficult to pick things up where you left them. Who would've thought?

There are still some things I want to fix and implement on this website, while also keeping it simple and light. I'll try and explain what and how in this post. Mind you: I'm absolutely no web developer or anything remotely like that.

<!--more-->

## Things I'd like to achieve with these updates
* introduce lazyloading and responsive images to make the photography pages *a lot* faster to load
* add a dropdown 'about' menu in the header; possible reworking the header system completely to utilize hugo's capabilities more
* re-style blogpost images to be more consistent
* built a way to make photo posts easier, using a function to range over the images and/or the concept of page bundles in hugo
* Look into web feed functionality
* Reach a state that I could describe as being fully functional (version 1.0)

All changes will also be documented on the [approriate page](/version)

## The idea of light-weight, susstainable webdesign
Resources, CO2 emissions from websites
Countered by low-tech solutions: static pages, no trackers etc, default fonts, lightweight images (haven't done that one yet)
https://solar.lowtechmagazine.com/2018/09/how-to-build-a-lowtech-website

## The solutions
### Page bundles
https://gohugo.io/content-management/page-bundles/
https://alison.rbind.io/post/2019-02-21-hugo-page-bundles/
https://www.ii.com/hugo-bundles/

### Responsive images

### Lazy lazy-loading
Lazy-loading comes built-in with the newest web browsers. I decided to make use of this so I could skip the whole java-script portion of my problem - the lazy way to introduce lazy-loading! The downside is that not all browser support this currently and some older browsers just never will. But ask yourself: why are you still using Internet Explorer?
https://nickmchardy.com/2020/05/adding-lazy-loading-for-images-in-hugo-static-site-generator.html
https://web.dev/native-lazy-loading/

### Dropdown menu's
I have a few pages that I like to share and that fit under my about page, so I wanted to include a drop-down menu for this. This meant harnassing the possibilities of the hugo menu templates and some messing about with css.

### Web feed functionality
https://gohugo.io/templates/rss/