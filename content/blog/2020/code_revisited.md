+++
title =  "The Code Revisited"
date = 2020-06-15T10:44:34+02:00
categories = ["hugo"]
featured_image = ""
description = ""
draft = true
+++

**Work in progress**

I've built this website almost a year ago during the summer days. This year, the summer arrived two months earlier than it is supposed to and this takes me back mentally to those days. Maybe that's why I've been looking into the behind-the-screens mess that is this blog. First lesson learned: letting things lie for long times will make it more difficult to pick things up where you left them. Who would've thought?

There are still some things I want to fix and implement on this website, while also keeping it simple and light. I'll try and explain what and how in this post. Mind you: I'm absolutely no web developer or anything remotely like that.

<!--more-->

## Things I'd like to achieve with these updates
* Built a way to make photo posts easier, using a function to range over the images and/or the concept of page bundles in hugo ✔
* Introduce lazyloading (and responsive images?) to make the photography pages *a lot* faster to load ✔
* Add a dropdown 'about' menu in the header; possible reworking the header system completely to utilize hugo's capabilities more ✘
* Re-style blogpost images to be more consistent ✘
* Look into web feed functionality ✘
* Rewrite 'About' page ✘
* Reach a state that I could describe as being fully functional (version 1.0) ✘

All changes will also be documented on the [approriate page](/version)

## The idea of light-weight, sustainable webdesign
Some time ago I stumbled upon [this article](https://solar.lowtechmagazine.com/2018/09/how-to-build-a-lowtech-website) from low-tech magazine about why and how to built 'low-tech' (probably more correctly called 'light-weight') websites.



Internet usage consumes a lot of energy and thus produces quite a lot of CO2 emissions. - Resources, CO2 emissions from websites
Countered by low-tech solutions: static pages, no trackers etc, default fonts, lightweight images (haven't done that one yet)

The only difficult thing for me to change here are the images; since it's partly a photo-blog I can't just start reducing the image quality completely without compromising the intention of the site. So there's three things I can do: 1) reduce the image quality to an acceptable level; 2) introduce lazy-loading so not every image has to be fetched, thus prevent loading them unnecessarily; and 3) make the images responsive so bigger images only get loaded when the user can make use of them.

## The solutions

### Image quality
I usually resize my images to 1200 pixels on the long side. This is, in my opinion, a good size to show off the picture. But what about file-size? As a sample: compressing a 1200 by 800 jpeg image with 100, 80 and 50 quality settings (in Adobe Lightroom) gives me files of 592 kB, 300 kB and 157 kB respectively. Lowering the image quality (which is the same as a higher level of jpeg compression) even a little can reduce file size significantly while having almost no visible impact. This is why I compress at least to 80 in Lightroom. From that point on, the impact can vary wildly depending on the image.

### Page bundles & shortcode
I made custom shortcode in layouts/shortcodes called photopost.html to range over all images inside of a given bundle:

```
{{ $myImage := .Page.Resources.Match "**.jpg" }}
{{ with $myImage }}
    {{ range . }}
        <img loading=lazy src="{{.Permalink }}">
    {{ end }}
{{ end }}
```

I still find it difficult to wrap my head around how all of this works in detail. I used [Regis' blogpost](https://regisphilibert.com/blog/2018/01/hugo-page-resources-and-how-to-use-them/) as starting point and adapted my code from there.

### Lazy lazy-loading
Lazy-loading comes [built-in](https://web.dev/native-lazy-loading/) with the newest web browsers. I decided to make use of this so I could skip the whole java-script portion of my problem - the lazy way to introduce lazy-loading! The downside is that not all browser support this currently and some older browsers just never will. But ask yourself: why are you still using Internet Explorer?

I used [this](https://nickmchardy.com/2020/05/adding-lazy-loading-for-images-in-hugo-static-site-generator.html) blog's code as a render hook to force all `<img>` tags to have the `loading=lazy` attribute.

### Responsive images
Imma skip this for now

### Dropdown menu's
I have a few pages that I like to share and that fit under my about page, so I wanted to include a drop-down menu for this. This meant harnassing the possibilities of the hugo menu templates and some messing about with css.

### Restyle blogpost images

### Web feed functionality
https://gohugo.io/templates/rss/