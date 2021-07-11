+++
categories = ["Internet"]
date = 2021-04-21T15:41:00Z
description = ""
draft = true
featured_image = ""
lastmod = 2021-07-11T16:55:00Z
title = "My ideal social network"

+++
The _nillies_ has been the decade of social media. From initial novelty to the digital equivalent of low-yield nuclear ICBM's. The analogy is maybe a bit over dramatic, but it's potential as a weapon has been demonstrated already. During these ten years, it has taken root almost everywhere on the globe. When older people started accepting it - and youngsters subsequently started to reject it in rebellion - was when it went from new frontier to established, settled fact.

I, too, was smitten by the ideas, rapidly accepting it as part of my (then fresh) university life.  But with growing awareness, both from myself as from society at large, about these social networks, their workings, consequences and ideology, came a desire, not to return to an earlier internet, but for a different way to do social networking. In this blogpost I'll try to explain my personal vision as a non-technical layman on what such a network would look like, where we can find existing inspiration and what pitfalls I think are to be avoided.

 <!--more-->

### Inspiration

The web isn't young or new anymore, how hard its sleek, turtlenecked proponents pretend it still is. There's a lot of material to work with here, technologies that have proven themselves, communities and sites that have come and gone, a whole legacy to build on. There's also some missed opportunities to embed certain technologies into the basic protocols that govern the web and that is something we have to deal with and be wary of for future development of the internet.

Somewhat before my time, but at the same moment, still one of the most basic forms of the internet, are personal websites. From basic HTML sites from the nineties, to GeoCities and basic blogging platforms, these gave you the tools to make your personal presence on the web.  This ideal of 'having your own place' seems to have faded and exchanged for a uniform experience for everyone. Even early social networking sites, such as MySpace, took their cues from the early web and let you make your own page, with obnoxious music that started playing automatically and garish backgrounds. These days, the personalisation is limited to strictly defined things such as an avatar, a profile banner (with specified dimensions) and maybe, if you're lucky, a background image.

(RSS)

One of the biggest successes of the dynamic 'Web 2.0' (as opposed to the earlier, static web) was WordPress, an free and open-source content management system that took the world by storm and actually drives around half of the websites even to this day. It's a great tool to build and manage a website, to be sure, but one of the most interesting features is its extensibility.

To me personally, one of the biggest inspirations was Tumblr. A (micro)blogging site that gave you a dashboard to scroll through all your subscribed to pages and a personal page that you could customize but filled automatically with your content - both original as 'reblogged' (content from other people you republished on your own page with a link back and sometimes with commentary). These personal pages were reminiscent of those earlier personal webpages. But I think my favorite feature is the simple follow button on these pages. Unobtrusive, this little button in the corner of the page is an aspiration for how both the 'old' personal websites and the 'new' social networks can be linked to each other.

More modern inspiration can be found in the Fediverse (federated networks), such as the Mastodon platform. This is a method of networking where not everything happens on the same website (such as is the case on all major websites with networking functions) but through a shared protocol. This way, different websites, with different goals, rules, communities, style or even (back-end) software can communicate with each other, freeing people from the restrictions of having only one such platform and even giving the possibility (but not necessity) of self-hosting.

### Must-have elements

From these inspirational forebears we can distills some elements that should be the core of this ideal social network I'm trying to imagine. It comes in the form of a software package, much like WordPress or Mastodon does, and not a specific website. On the contrary, what I want is a network _of_ websites, instead of a network _on_ a website. 

Firstly, it should be free and open-source. I don't have any qualms with commercial or proprietary software _per se_, but there should be a base package that gives universal access to online social networking. Although I'd prefer it to have a copyleft license, making derivative works equally free, I don't think it's a hard must.

Maybe more fundamental, would be the protocol itself that defines its usage and implementation. The (FOSS) software itself could be limited to a basic reference tool, so that alternatives could be built that are equally compatible. There should be enough distance between the institution that governs this protocol and whoever implements the reference software, so that feature creep doesn't sideline alternative implementations.

Secondly, some sort of federation should be possible. This gives users sovereignty over their own data\[^1\] by allowing multiple access-providers, which have to have or earn the users' trust or even self-hosting, taking responsibility for oneself (or others) in one's own hands.

Federation also allows for a nuanced approach to content moderation, social rules, potential monitization of the service or which set of extensions will be accepted. This is also one of the possible pillars around which communities form: users with shared expectations can join the same provider, but still interact with users outside their community within the constraints this community or its provider sets out. To facilitate this, a robust migration system should be implemented so that one can change provider without too much of a hassle (such as losing data or connections to other users).

The protocol should be fairly extensible, in that different kinds of data can be shared among users, depending on their own choices and preferences. This is what think of as the modularity of a general social network. What this means is that one person can decide to share a specific set of datatypes, while the other person accepts another. For instance: person A shares pictures, music and events, while person B, who subscribes\[^2\] to A, is only interested in their pictures. On the other hand, B also shares additional datatypes, such as news articles, which A wants to see, even though they themselves don't use that particular datatype. Furthermore, B shares some personal information with friends that they don't want A to have access to, so they are automatically barred access to this data. This should work both on the level of the subscriptions (one chooses what set of datatypes will be followed and one can access what set a follower has access to), as on the level of the account itself (maybe the focus of the account is on photography and there's no need to share or accept any other data besides those pictures), and possibly on the level of the provider too (this is more in line with the current model where social networks limit themselves to one specific format). 

Some datatypes could be implemented as recognized standard data types outside of the base protocol. Additional features beyond its scope should be implemented through these kind of extensions. 

And last but not least, it should have a focus on ease of access. This can be done by having a basic dashboard to manage the network and a way to use and share templates for the personal pages itself (à la Tumblr). Most importantly, by using federation the technical hurdle of installing, running and using the back-end software can be skipped by having the aforementioned network providers (be it communities, individuals, companies, cooperations, what have you) deal with that. Much like how most current corporate social networking services offer the experience to it's users, who don't have to deal with the technicalities, but with the added bonus of giving users the _choice_ of how much access they do want to what's under the hood. Some users just want to post data, while others love to tinker with the presentation of their site, while even more hardcore users want full control over the network. The idea is that there any user on the technical-involvement-spectrum should be able to join and enjoy the same access.

### What is to be avoided

Commercialism embedded into the core system.

(Forced) profile fragmentation, only limited to sensible compartmentalization. 

### A mock-up

A collection of (personal) webpages, a local dashboard that fetches wanted information from the services you subscribed to.

\[^1\]: Although this is only one part of tackling the problem of data harvesting. It does nothing to stop the harvesting of behavioral data that is generated by use.

\[^2\]: I'm called it subscription to keep it general. These could be acquaintances or friends, but also pages from bands, places, brands, companies, etc... 