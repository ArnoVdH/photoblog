+++
categories = []
date = 2021-10-23T22:00:00Z
description = ""
draft = true
featured_image = ""
title = "Setting up Rclone"

+++
Rclone is a versatile and powerful command-line utility for managing cloud storage.

Here I am using it to manage my own cloud storage with pCloud.

I have it set-up on my desktop pc, but haven't made it sync with my notebook, nor was my rudimentary way of emulating a continuous synchronisation done in a satisfactory way (it synched at startup and every few minutes, but shutting down before an automated sync happened made me lose my changes).

<!--more-->

### Installing & setting up Rclone

Installing Rclone is as simple as downloading it from the official repositories of your chosen distro. In my case, I just use \`sudo pacman -S rclone\` in the terminal, and a few short seconds later the real work of configuring my setup can start.

I use three folders: a default cloud one that's encrypted, a public one for sharing files with other people and a mobile one, for syncing with my mobile (Android) devices on which it's more difficult to do a similar setup because of the restrictions on a stock Android OS. The configuration for all three of these would be similar, so I'm just going to describe the one for my general cloud storage.

### Encrypting

### Synching

I want to set up rclone as a small, lightweight cloud synchronisation system, without the need for a dedicated app from pCloud themselves (which also doesn't give me a way to encrypt my data without an extra fee)

#### Cronjob

#### At shutdown