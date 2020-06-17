+++
title =  "Anne"
date = 2020-05-10T11:00:00+02:00
tags = ["portrait", "digital", "Canon 70D"]
series = []
featured_image = "/img/2020/Anne1/anne-2.jpg"
description = ""
draft = true
+++

(hier moet shortcode komen)

***

Inline hugo code:
{{ with .Resources.ByType "image" }}
{{ range . }}
{{ .RelPermalink }}
{{ end }}
{{ end }}


***

Hieronder afbeeldingen in bundle:

![](/photo/2020/AnnePortraits/anne-1.jpg)

![](/photo/2020/AnnePortraits/anne-2.jpg)

![](/photo/2020/AnnePortraits/anne-3.jpg)


***

Hieronder afbeeldingen in static:

![](/img/2020/Anne1/anne-1.jpg)

![](/img/2020/Anne1/anne-2.jpg)

![](/img/2020/Anne1/anne-3.jpg)