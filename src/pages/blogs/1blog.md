---
title: 1st Blog
author: Alec Singer
description: The first blog post! This is the one where I setup my website and so all the cool ssh stuff :)
layout: ../../layouts/BlogLayout.astro
---

# 1st Blog

### This is the first blog!

## Start of the class:

The start of the class was nice and chill for me, as I spent the first few days setting up WSL (Windows Subsystem for Linux) on my laptop. I also got connected to the sandbox server. Later in the week, I started to research various static site options to host this very blog!

## Static Site:

After some research, I settled on using the Astro framework because of it's lighting fast compile time and default markdown support (that's what these blogs are written in).  I first setup my basic pages, then created a static header bar component and a custom layout so I could apply CSS universally. I setup the blogs page to automatically import and list all the markdown pages, including adding title and description.

In my own time, I messed around with CSS for a while, so the site could look diffrent from default uncolored HTML. I also setup an SSH key on the server, so I could authenticate/connect to the server faster. This allowed me to make a custom NPM script that uploaded my site straight to the server. 

Script: (actually just an rsync command in the package.json):

```"upload": "rsync -arvI --delete ./dist/ alec.singer@sandbox.sonomaacademy.org:/home/alec.singer/public_html", ```

Afterwords I used a bit of AI to redesign the frontend of the site. I added a background grid, and attempted to add custom animations as well, but I was unable to find a performant solution.

