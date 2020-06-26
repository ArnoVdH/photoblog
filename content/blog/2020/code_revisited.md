+++
title =  "The Code Revisited"
date = 2020-06-15T10:44:34+02:00
categories = ["hugo"]
featured_image = ""
description = ""
draft = false
+++

**Work in progress**

I've built this website almost a year ago during the summer days. This year, the summer arrived two months earlier than it is supposed to and this takes me back mentally to those days. Maybe that's why I've been looking into the behind-the-screens mess that is this blog. First lesson learned: letting things lie for long times will make it more difficult to pick things up where you left them. Who would've thought?

There are still some things I want to fix and implement on this website, while also keeping it simple and light. I'll try and explain what and how in this post. Mind you: I'm absolutely no web developer or anything remotely like that.

<!--more-->

## Things I'd like to achieve with these updates
* Built a way to make photo posts easier, using a function to range over the images and/or the concept of page bundles in hugo ✔
* Introduce lazyloading and lower image file size to make the photography pages *a lot* faster to load ✔
* Add a dropdown 'about' menu in the header ✔
* Re-style blogpost images to be more consistent ✔
* Re-write css ✔
* Adapt header to use favicon ✔
* Look into web feed functionality ✔
* Rewrite 'About' page ✔
* Reach a state that I could describe as being fully functional (version 1.0) ✘

All changes will also be documented on the [approriate page](/version).

## The idea of light-weight, sustainable webdesign
Some time ago I stumbled upon [this article](https://solar.lowtechmagazine.com/2018/09/how-to-build-a-lowtech-website) from Low-tech Magazine about why and how to built 'low-tech' (probably more correctly called 'light-weight') websites.

Although the internet seems immaterial, it costs energy to store and use all its information. Huge datacenters that consume equally huge amounts of energy (both for the the server-racks as the cooling systems) that run 24/7 serve us with websites everytime we ask for it. A huge part of the internet is *dynamic* these days. That is to say: they assemble the site at the moment of request, with input from underlying databases; think WordPress or Facebook, both running PHP. Dynamic webdesign has many advantages, but isn't always necessary. Static websites are 'older' technology that just serve the files that are stored on the server - no server-side assembling required, reducing the amount of computing power (and thus energy) required. The last few years these kind of websites have been making a comeback with the help of static website generators that drastically expand the tools to make a large static website that would otherwise be too labour-intensive to make. Generators like this include [Jekyll](https://jekyllrb.com/), [Pelican](https://blog.getpelican.com/), [Gatsby](https://www.gatsbyjs.org/) and [Hugo](https://gohugo.io/), which is what I'm using.

So besides hosting a static website, there are other things that could be done to minimize unnecessary energy usage, without sacrificing readability or design. Such as using the default typeface (so no unnecessary fonts have to be downloaded), reduce the amount and size of images and general reduction of files, code and bloat. I use no JavaScript for instance, both because I don't really know how to use it but also because it would add an axtra layer of files. The most interesting measure though, I think, is to remove tracking, cookies and advertisments. This means no analysis software too, but some honest introspection and humility should be enough to know that for a lot of personal sites and blogs this does not matter in the slightest. You *could* go further and self-host your server, in which case you would have access to the same data to make your own analysis.

The only difficult thing for me to change here are the images; since it's partly a photo-blog I can't just start reducing the image quality completely without compromising the intention of the site. So there's three things I can do: 1) reduce the image quality to an acceptable level; 2) introduce lazy-loading so not every image has to be fetched, thus prevent loading them unnecessarily; and 3) make the images responsive so bigger images only get loaded when the user can make use of them.

## The solutions

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

I used [this](https://nickmchardy.com/2020/05/adding-lazy-loading-for-images-in-hugo-static-site-generator.html) blog's code as a render hook to force all `<img>` tags to have the `loading=lazy` attribute. The code worked on the local server but didn't when deployed. Luckily I also integrated a lazy-loading attribute into my photopost shortcode so all those images at least get the lazy-loading treatment.

### Image quality
I usually resize my images to 1200 pixels on the long side. This is, in my opinion, a good size to show off the picture. But what about file-size? As a sample: compressing a 1200 by 800 jpeg image with 100, 80 and 50 quality settings (in Adobe Lightroom) gives me files of 592 kB, 300 kB and 157 kB respectively. Lowering the image quality (which is the same as using a higher level of jpeg compression) even a little can reduce file size significantly while having almost no visible impact. This is why I compress at least to 80 in Lightroom. From that point on, the impact can vary wildly depending on the image.

For good measure I passed all my photographs through another round of compression to shave off an additional 45%, give or take. This *halved* the load of the home page!

### Dropdown menu's
I have a few static pages that I like to share and that fit under my about page, so I wanted to include a drop-down menu for this. This meant going back to hugo menu templates. I added a new menu type (called 'about') to range over as a submenu. Then I used some (probably very sloppy) css code to position this menu under 'About' and make it hidden unless when hovered over.

### Restyle blogpost images
These were just images flung into the post until now, sometimes with a little caption that didn't quite line up. I started using the 'figure' shortcode so I could add captions easily and add classes.

### Rewrite CSS
Man, what a nightmarish mess this is, even after rewriting it all. I changed how a few things are handled without changing the design of my blog too much.

### Favicon
Made a simple typographical favicon to make the website recognizable in a browser tab. I converted this through a [favicon generator](https://realfavicongenerator.net/) and added some of the files (the .ico and .png files to be precize) to my static folder and added the necessary code to my head.html template.

### Rewrite the About page
[See for yourself.](/about) Less links to scattered page, those can now be easily found and reached through the dropdown menu's described above.

### Web feed functionality
Hugo has a simple built in [rss page template](https://gohugo.io/templates/rss/). I just put the relevant code in the head.html file to get it to work. From now on my blog can be subscribed to!

### Conclusion
From now on this isn't just a 'technically functional website' but one that I can say is 'done'. That isn't to say that there are not more improvements or additions to be made, but none are necessary to have the site do what I want it to do.