+++
title = "My ideal social network"
categories = ["Internet"]
date = 2021-07-11T14:00:00Z
description = ""
draft = false
featured_image = ""
lastmod = 2021-08-23T17:00:00Z
+++
The _nillies_ has been the decade of social media. From initial novelty to the digital equivalent of low-yield nuclear ICBM's. The analogy is maybe a bit over dramatic, but it's potential as a weapon has been demonstrated already. During these ten years, it has taken root almost everywhere on the globe. When older people started accepting it - and youngsters subsequently started to reject it in rebellion - was when it went from new frontier to established, settled fact.

I, too, was smitten by it all, rapidly accepting it as part of my (then fresh) university life.  But with growing awareness, both from myself as from society at large, about these social networks, their workings, consequences and ideology, came a desire, not to return to an earlier internet, but for a different way to do social networking. In this blogpost I'll try to explain my personal vision as a non-technical layman on what such a network would look like, where we can find existing inspiration and what pitfalls I think are to be avoided.
 <!--more-->
## Inspiration
The web isn't young or new anymore, no matter how hard its sleek, turtlenecked proponents pretend it still is. There's a lot of material to work with here, technologies that have proven themselves, communities and sites that have come and gone, a whole legacy to build on. There's also some missed opportunities to embed certain technologies into the basic protocols that govern the web and that is something we have to deal with and be wary of for future development of the internet.

Somewhat before my time, but still one of the most basic forms of the internet, are personal websites. From basic HTML sites from the nineties, to GeoCities and basic blogging platforms, these gave you the tools to make your personal presence on the web.  This ideal of 'having your own place' seems to have faded and was exchanged for a uniform experience for everyone. Even early social networking sites, such as MySpace, took their cues from the early web and let you make your own page, with obnoxious music that started playing automatically and garish backgrounds. These days, the personalisation is limited to strictly defined things such as an avatar, a profile banner (with specified dimensions) and maybe, if you're lucky, a background image.

One of the biggest successes of the dynamic 'Web 2.0' (as opposed to the earlier, static web) was WordPress, an free and open-source content management system that took the world by storm and actually drives around half of the websites even to this day. It's a great tool to build and manage a website, to be sure, but one of the most interesting features is its extensibility.

To me personally, one of the biggest inspirations was Tumblr. A (micro)blogging site that gave you a dashboard to scroll through all your subscribed to pages and a personal page that you could customize but filled automatically with your content - both original as 'reblogged' (content from other people you republished on your own page with a link back and sometimes with commentary). These personal pages were reminiscent of those earlier personal webpages. But I think my favorite feature is the simple follow button on these pages. Unobtrusive, this little button in the corner of the page is an aspiration for how both the 'old' personal websites and the 'new' social networks can be linked to each other.

More modern inspiration can be found in the Fediverse (federated networks), such as the Mastodon platform. This is a method of networking where not everything happens on the same website (such as is the case on all major websites with networking functions) but through a shared protocol. This way, different websites, with different goals, rules, communities, style or even (back-end) software can communicate with each other, freeing people from the restrictions of having only one such platform and even giving the possibility (but not necessity) of self-hosting.

## Must-have elements
From these inspirational forebears we can distills some elements that should be the core of this ideal social network I'm trying to imagine. It comes in the form of a software package, much like WordPress or Mastodon does, and not a specific website.[^1] On the contrary, what I want is **a network _of_ websites, instead of a network _on_ a website.**

Firstly, it should be free and open-source. I don't have any qualms with commercial or proprietary software _per se_, but there should be a base package that gives universal access to online social networking. Although I'd prefer it to have a copyleft license, making derivative works equally free, I don't think it's a hard must.

Maybe more fundamental, would be the protocol itself that defines its usage and implementation. The (FOSS) software itself could be limited to a basic reference tool, so that alternatives could be built that are equally compatible. There should be enough distance between the institution that governs this protocol and whoever implements the reference software, so that feature creep doesn't sideline alternative implementations.

Secondly, some sort of federation should be possible. This gives users sovereignty over their own data[^2] by allowing multiple access-providers, which have to have or earn the users' trust or even self-hosting, taking responsibility for oneself (or others) in one's own hands.

Federation also allows for a nuanced approach to content moderation, social rules, potential monitization of the service or which set of extensions will be accepted. This is also one of the possible pillars around which communities form: users with shared expectations can join the same provider, but still interact with users outside their community within the constraints this community or its provider sets out. To facilitate this, a robust migration system should be implemented so that one can change provider without too much of a hassle (such as losing data or connections to other users).

The protocol should be fairly extensible, in that different kinds of data can be shared among users, depending on their own choices and preferences. This is what think of as the modularity of a general social network. What this means is that one person can decide to share a specific set of datatypes, while the other person accepts another. For instance: person A shares pictures, music and events, while person B, who subscribes[^3] to A, is only interested in their pictures. On the other hand, B also shares additional datatypes, such as news articles, which A wants to see, even though they themselves don't use that particular datatype. Furthermore, B shares some personal information with friends that they don't want A to have access to, so they are automatically barred access to this data. This should work both on the level of the subscriptions (one chooses what set of datatypes will be followed and one can access what set a follower has access to), as on the level of the account itself (maybe the focus of the account is on photography and there's no need to share or accept any other data besides those pictures), and possibly on the level of the provider too (this is more in line with the current model where social networks limit themselves to one specific format). 

Some datatypes could be implemented as recognized standard data types outside of the base protocol. Additional features beyond its scope should be implemented through these kind of extensions. 

And last but not least, it should have a focus on ease of access. This can be done by having a basic dashboard to manage the network and a way to use and share templates for the personal pages itself (à la Tumblr). Most importantly, by using federation the technical hurdle of installing, running and using the back-end software can be skipped by having the aforementioned network providers (be it communities, individuals, companies, cooperations, what have you) deal with that. Much like how most current corporate social networking services offer the experience to it's users, who don't have to deal with the technicalities, but with the added bonus of giving users the _choice_ of how much access they do want to what's under the hood. Some users just want to post data, while others love to tinker with the presentation of their site, while even more hardcore users want full control over the network. The idea is that there any user on the technical-involvement-spectrum should be able to join and enjoy the same access.

## Pitfalls
The main thing we don't want is a commercial logic driving the networks. It's this commercial incentive that drives the development of manipulative algorithms and data harvesting. The network should be secure, private and neutral by default.

Algorithmic curation of the generated feed in the dashboard isn't problematic in itself, as long as it's used voluntarily and it's clear what the algorithm does. This could be achieved with plugins instead of being built into the core system.

Not only the software itself should be non-commercial, but the government of the protocol as well. It should be the users (or at least representatives) that decide the direction of the network, not the companies trying to use the protocol for their own gain.

Another thing that should be avoided is the forced profile fragmentation. What I mean by this, is the need to make a new profile for every type of social network profile you want to have. This is of course because in the current system of corporate social media, every site is their own walled garden, and this is especially relevant for the sites with specific subject matter. For now, the Fediverse seems to develop along similar lines, but this is partly because of the huge effort it requires to develop one aspect of a social network, especially with almost exclusively voluntary labor, and partly because they're stuck, so to speak, in the paradigm. A modular network, as described above, could help aleviate this.

That isn't to say that compartmentalization of profiles shouldn't be possible, far from it. There are good reasons for one to want to do that, but it shouldn't be forced. People who don't want to fragment their network shouldn't have to do that just because they want to share books with friends and site X doesn't allow that while people who would be interested in these book recommendations but aren't prepared to make *yet another* account on some site Y won't be able to see it.

Let users decide what to share, what to view and who gets to see what.

## Mockup
To be clear, what I'm imaging is as follows:

* A general protocol
* A FOSS implementation of said protocol

This software package would consist of the following:

* Self-hostable back-end
* Federation
* Personal webpages with easy-to-follow communication
* Different levels of customizability, from casual users, to geeks, to artists, to professional webdesigners
* Multiple datatypes and ways to limit and select different sets of them for different users
* Control over what data is public and to what extent
* Some sort of encryption between users to keep private data really private (and not just 'not shown')

Some examples:

* You make an account on the instance of your locality (neighbourhood, town, maybe country) and only use the default capabilities, you don't need anything more for your purposes. Your personal page has the basic layout and colorscheme chosen by your provider and have a range of basic datatypes: text, links (to articles), image-sharing, comments on posts and the like. You're up and running in no time and have everything at your disposal.
* You go to the page of a acquintance, which uses a popular, clean-looking template. This person uses this mainly as a general social media profile. You click on a small icon in the upper-right corner of the page (or maybe even a button in your browser itself) and a little menu appears showing the different kinds of data in a checklist. Clicking again on the same button accepts them all and you subscribed to the person. But since you're just interested in this person's pictures, you deselect all other data and confirm
* You're scrolling through your personal feed when you see a notification that someone you really like subscribed to your profile. You decide to grant them access to more personal data, such as pictures where you're partying
* You follow a podcaster who also uses the same profile for things like branding, Q&A sessions with fans and some other things. Luckily, the podcastplayer you use has access to your profile and only looks for the relevant links to the episodes.
* You want more ways to find out about new pages, so you download or activate a new extension that shows you posts from other pages or recommendations. This could be done through curated lists that you subscribe to seperately.
* While reading your feed, you bump into some vile comments on someone else's profile. You notice that the whole instance[^4] is something you'd rather not see. You click open the moderation menu and decide to block the provider itself from appearing on your feed. This could go even further: a whole community could decide to defederate from problematic hosts and exclude them from the local network.
* Your provider has blocked a domain but you disagree with this community-made decision. You decide to migrate to another instance where the rules are more to your liking and with a few simple clicks, your account has moved to the new place, with all data, customization and connections intact (where applicable).
* You're not that active on the network, you mainly follow people without posting a lot of stuff yourself. You decide you only need to periodically update your personal page (maybe with an inspirational quote?) and make it so that it's a purely static page, since there's no need for  live comments or updates.
* You follow an organisation that holds regular parties in your town and you subscripe to their page. You yourself don't host public parties, but nonetheles you can join the event pages they make and let them know you're coming. Maybe with a seperate extension you can even keep your own calendar up to date with everything there is to do?

## Conclusion
This is all pretty vague, I'm aware of it. I don't really have any idea of the feasibility, possible limits. And many of the ideas are already existing in one way or another. I'm not reinventing the wheel here. Following people, dashboards, federation (the most interesting idea for the future of the web at the moment!), it all exists, but not in some comprehensive form.

My question to myself, originally, was why we don't have a social network built around these personal pages of the past, augmented with the social media innovations of the last 15 years? Some sort of peer-to-peer social networking, as it were. But one of the problems here is that not enough people are actually interested in building and maintaining their own personal web page, let alone manage the whole hosting of it. By using federation this divide can be bridged by letting people choose between joining a community or self-hosting, so (self-hosted-)peer-to-peer or (self-hosted-)peer-to-community communication is possible.

Thoughts, critiques, questions, suggestions, all are very welcome!

[^1]: This seems to imply the use of dynamic websites, which are more computationally intensive compared to static ones (that just serve some pre-determined files, mostly HTML, CSS and javascript), thus more energy demanding. I think it would be technically possible to have a locally running dashboard while the personal page is constructed as a static one.

[^2]: Although this is only one part of tackling the problem of data harvesting. It does nothing to stop the harvesting of behavioral data that is generated by use.

[^3]: I'm calling it subscription to keep it general. These could be acquaintances or friends, but also pages from bands, places, brands, companies, etc... 

[^4]: Also called a server, a pod, a host,... A localized version of the software run by a specific provider.
