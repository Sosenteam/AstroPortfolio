---
title: 3rd Blog
author: Alec Singer
description: Godot 2, Electric Boogaloo
layout: ../../layouts/BlogLayout.astro
---

# 3rd Blog: More Godot

## Godot Practice

This week I started working on my next practice game, which is a top-down dungeon crawler. I mainly made this project because I wanted to practice working with new nodes like TileMapLayer, Camera2D, NavigationAgent and more. I started by making a basic player, with features like movement, dashing and a cooldown system.

## State Machines

After setting up basic movement and controls for my game, I found a [great tutorial](https://www.gdquest.com/tutorial/godot/design-patterns/finite-state-machine/) focused on state machines. State machines basically allow you to split your code into seperate 'states', where only one state is running at any given time. For my movement system, the states I used are "Idle","Moving" and "Dashing". I also added a combat statemachine that has the states: "IdleAttack","LightAttack" and "HeavyAttack". This was my first time using state machines for a player controller.

![NodeTreeOfStateMachines](/alec.singer/statemachinenodes.png)


## Cameras and Tilemaps

My first problem with my game was the player would quickly move offscreen, and it was hard to track it's movements. I fixed this by using a Camera2D node on my player, which kept the player permanently centered. 

The next feature I added was a background tilemap, using a TileMapLayer node. This tilemap was very hard to configure, as I'm still learning how to make tilemap terrains (autotiling). Eventually I was able to make a terrain for the outside walls, including collision and naviation polygons. I also added a seperate tilemap terrain for the ground, without any collision. 

![Image no workie](/alec.singer/tilemap.png)


## Enemies and Navigation 

Finally I added a ghost enemy to my game, and my goal was to make it constantly chase the player. I achieved this by using a NavigationAgent node on the ghost, and making navigation polygons for each of the tiles in my tilemap. I had a few issues getting the speed of the ghost to be slower than the player, but it was just a problem with not using delta in the movement script.  

I also started working on an attack and invincibility-frame system, but I didn't have time to finish it this week.

![Image no workie](/alec.singer/ghost.png)
