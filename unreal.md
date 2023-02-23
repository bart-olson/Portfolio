---
layout: default
title: Unreal Engine Work
permalink: /unreal/
---

<h2 style="text-align:center;">Voxel Plugin  </h2>
<p style="text-align:center;">Voxel Plugin (VP) is a plugin produced by a small team for Unreal engine. It implements the 'marching cubes' algorithm to generate voxel terrain that can be manipulated in a wide variety of ways. For anyone curious and looking into VP, they released the first version a few years ago, which is when I purchased it. That version is 1.2, has full documentation, and is just barely still supported for Unreal 5. However the team decided that 1.2's structure was a little short-sighted and unwieldy, and is currently working on 2.0 which is still in beta. The project is totally independent from 1.2, but you will own it you purchase 1.2. Since it's in beta, it has virtually no documentation save for a discord server and a roadmap. This makes it very fun to work with! 

That being said, I chose a voxel plugin because I really enjoy games with voxels: Dwarf Fortress is the OG in that regard, closely followed by Minecraft. I see games like Astroneer and Deep Rock Galactic as loose spiritual successors, since you're given full ownership of the map with much higher resolution voxels. I think voxel games hold a lot of promise, and provided new algorithms are created to solve problems like generating and modifying the terrain, and applying physics to loose terrain pieces, I believe a lot of games and genres will start to adopt the system. That level of immersion can only be achieved when you can do anything you want to the landscape!  </p>



<h2 style="text-align:center;">Landform generation  </h2>
<p style="text-align:center;">If you've looked at my Blender page, you know I love procedural generation, and I like thinking about how to apply it properly! There's plenty of places that there's too much procedural generation and the whole feel becomes kind of bland - but a careful ratio of procedural generation to points of interest and hand-crafted assets can not only reduce workload for developers, but endlessly explorable worlds for players! 

VP has standard noise nodes already, with plans to build more in the future. These can be combined with several other tools that set the plugin apart from a simple terrain generator. The two I'm most interested in are Voxel Landmass Actors and Voxel Heatmaps

Voxel landmass actors take in a static mesh, then convert it into voxels - meaning you can spawn any static mesh into this system and get landscape voxels returned! I'm still playing with the voxel resolution, since a lot of the meshes even when they're the size of a house still don't quite look like what they're supposed to look like. (Maybe this is why they're meant to be used as landscape). I was also interested in using landmass actors as spells in a fantasy game - you can spawn a landmass actor, then move it across the terrain to create interesting bulges and mounds as the VP melds with it. The problem is that it's really resource intensive running the whole chunk back through the marching cubes algorithm. I think that the way around this for now is to animate with a static mesh a spell, then when the spell 'finishes' spawn a static mesh and occlude the transition in particle effects. For example, if you were to cast a spell that shoots or spawns a stalactite - it flies toward the enemy as a static mesh with a texture and particle effects, then when it strikes the terrain it spawns another static mesh to represent the resulting impact. I should really make that, that sounds like a sweet demo for the website! 

Next up is the Voxel Heatmap, which I'm really excited to use more. The basic concept is that you can build a .png heatmap using something like Photoshop or Blender, then import that and connect it to the Voxel Heatmap object, then spawn that on top of your terrain. It doesn't just replace the terrain though, it melds with it like a Voxel Landmass Actor described above, so that means you can use different organizations and setups of heatmaps in one piece of terrain. This is key to keeping procedural generation interesting, I think. You can combine elements of hand-construction with elements of procedural generation to get the right mix. I'll go over it in a later section, but masking the terrain in different ways will lead to a lot of options for building interesting terrain. Cave generation (probably via splines) is not in VP yet, but should be coming 'back' soon since it was in before. Did I mention it's in beta?  </p>

<h2 style="text-align:center;">Foliage Masking  </h2>
<p style="text-align:center;">Foliage masking is a really cool feature of VP. I actually assumed that Unreal Engine had something similar built in, but it appears they don't, which sort of makes Voxel Plugin's feature even cooler! The concept is pretty simple - You can mask an area of terrain based on it's (x,y) positions using any kind of math - x-position, y-position, both, x,y,z position, and any number of equations. Chiefly this will be used to create biomes of different kinds - by masking both terrain type and foliage, you can generate procedural landscape as far as you want, just like Valheim! Here's some experiments I've done so far on this concept, and the relevant parts of the graph, in case you're here to look at that.  </p>

<h2 style="text-align:center;">Runtime Terrain Deformation  </h2>
<p style="text-align:center;">This is especially interesting to me - it's what's expected from a voxel plugin, but there's really endless options for a game that has it in terms of ways to use it. My goal is to eventually build a game that has a large number of magic spells that are used to deform/destroy/build on terrain. Imagine Deep Rock Galactic, but it was a multiplayer spell battle game!   </p>

<h2 style="text-align:center;">Landscape Materials  </h2>
<p style="text-align:center;">  </p>

<h2 style="text-align:center;">General Gamedev stuff  </h2>

<h3 style="text-align:center;">Inventory and Interaction System  </h3>
<p style="text-align:center;">Tutorials used and why  </p>

<h3 style="text-align:center;">AI  </h3>
<p style="text-align:center;">  </p>

<h3 style="text-align:center;">  </h3>
<p style="text-align:center;">  </p>



<h2 style="text-align:center;">  </h2>
<p style="text-align:center;">  </p>

Here's a page that will have stuff about Unreal engine  

[Home](https://bart-olson.github.io/Portfolio/)