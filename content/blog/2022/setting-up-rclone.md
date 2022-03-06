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

I have it set-up on my desktop pc, but haven't made it sync with my notebook, nor was my rudimentary way of emulating a continuous synchronization done in a satisfactory way (it synced at startup and every ten minutes or so, but shutting down before an automated sync happened made me lose my changes).

For this little exercise I'm going to assume I just want one folder synced with the cloud on my notebook. I'm not going to use an encrypted storage here, but that that is also an built-in possibility with rclone.

### Installing & setting up Rclone

Installing Rclone is as simple as downloading it from the official repositories of your chosen distro. In my case, I just use \`sudo pacman -S rclone\` in the terminal, and a few short seconds later the real work of configuring my setup can start.

Let's start by running rclone config in the terminal.

### Synching or mounting?

I want to set up rclone as a small, lightweight cloud synchronization system, without the need for a dedicated app from pCloud themselves (which also doesn't give me a way to encrypt my data without an extra fee). There are multiple ways to achieve this.

Firstly, you can use the rclone sync command to make a local folder and the remote folder synchronize. That way, there is an exact copy on your system. This command can be run manually or with the use of a cronjob (at startup and at certain intervals for instance). This is how I had it originally set up.

Another way would be to use the rclone mount command to mount the remote to your filesystem. This is also achieves our goal of having the remote accessible _but_ may have some downsides with reliability. To counter this, we'll use caching.

### Setup daemon with systemd

Because we mounted our remote, we need to setup the daemon. We'll do this through systemd.