---
title: 2nd Blog
author: Alec Singer
description: Godot! Godot! Godot! Godot! Godot! Godot! Godot!
layout: ../../layouts/BlogLayout.astro
---

# 2nd Blog: Godot Edition

## Game Engine / Jam Search

I started by looking through Itch.io for possible game jams, and although there were hundreds, it was quite hard to find any with more than ~10 people that lasted more than 3-4 days. The one game jam I had heard of was Brackeys Game Jam, but it was only 4 days long.

I also looked at a few basic game engines, including [CT.JS](https://ctjs.rocks/) (based on PixiJS), P5/Q5.js, and finally [Godot](https://godotengine.org/). I was immediately drawn to Godot because of how many existing/popular games were made with it and because its Python-like syntax was interesting to me. Before this class, I'd gone through 2 short Godot tutorials, but I never dove deep enough to learn the core engine concepts. 

## Godot, Godot, Godot!

I started by doing the ["Dodge the creeps"](https://docs.godotengine.org/en/stable/getting_started/first_2d_game/index.html) tutorial project in the Godot docs (which I did ~1 year ago), which was great for refreshing/practicing my GDScript syntax. After this tutorial, I dove into the docs (mostly in my free time). I read through the entirety of the core concepts section, then the 2D section, in addition to reading about specific mechanics, including autoloads, collision, changing scenes, input, and much more.  

Coming off of the weekend, I started by making a super simple pong game, though I had some struggles with manually moving 2DRigidBodies. After that, I built a simple demo that acted like a pool video game, in which you drag opposite from the direction you want the ball to go. I also added other balls that the main cue ball could collide with.

Finally, I've started working on building a mini-golf game, based on the basic drag-to-move mechanic from the pool game, but with much more complexity. First I changed the simple direction line into a full arrow, and I was able to get it fully isolated in the ball scene, rather than needing to be in the main scene. Next, I made it so the ball would naturally slow down and made the arrow's length small enough that you could still get a full-power hit with a smaller screen size.


![Image no workie](/alec.singer/golfimage.png)

My next step was adding tilemaps so each level could be built without requiring tons of individual nodes for the background/walls. After setting up a basic background map, I added custom collision to the foreground tilemap layer. I also made a separate "hole" scene that would trigger the loading of the next level. I added this scene to a scene collection in the foreground tilemap layer, so it can be placed automatically without needing me to add it for each level.

![Image no workie](/alec.singer/golfvideo.webp)


## Git, SSH & Git Godot Plugin

After getting this far with my game, I thought it would be nice to find an easy solution for connecting Git to Godot. I spent a few hours messing with the Git Godot plugin, including setting up SSH keys and even a PAT (personal access token), but I was unable to get the plugin to work consistently (not on my laptop at least). 

I think the next best option for using Git is to use a basic GUI tool like [fork.dev](https://fork.dev/) or just the basic CLI, as a separate window outside of Godot.