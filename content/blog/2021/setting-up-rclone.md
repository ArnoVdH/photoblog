+++
categories = []
date = 2021-10-23T22:00:00Z
description = ""
draft = true
featured_image = ""
title = "Setting up pCloud sync with Rclone"

+++
[Rclone](https://rclone.org/) is a versatile and powerful command-line utility for managing cloud storage. It's available for all major operating systems and I'm using it on Linux. Specifically, I am using it to manage my own cloud storage with [pCloud](https://www.pcloud.com/eu).

<!--more-->

I have it set-up on my desktop pc, but haven't made it sync with my notebook, nor was my rudimentary way of emulating a continuous synchronization done in a satisfactory way (it synced at startup and every few minutes, but shutting down before an automated sync happened made me lose my changes).

For this little exercise I'm going to assume I just want one folder synced with the cloud on my notebook. There's already an encrypted storage on there, originally setup from my desktop, but that shouldn't matter for how to go about this.

### Installing & setting up Rclone

Installing Rclone is as simple as downloading it from the official repositories of your chosen distro. In my case, I just use \`sudo pacman -S rclone\` in the terminal, and a few short seconds later the real work of configuring my setup can start.

Let's start by running rclone config in the terminal.

### Encrypting

### Synching

I want to set up rclone as a small, lightweight cloud synchronisation system, without the need for a dedicated app from pCloud themselves (which also doesn't give me a way to encrypt my data without an extra fee)

#### Cronjob

#### At shutdown