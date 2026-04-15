---
layout: default
modal-id: noise1
date: 2025-04-08
img: noise.jpg
alt: image-alt
project-date: April 2026
client: Start Bootstrap
category: Unreal Engine 5, C++, Tools, Editor Widget
description: Use this area of the page to describe your project. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Mollitia neque assumenda ipsam nihil, molestias magnam, recusandae quos quis inventore quisquam velit asperiores, vitae? Reprehenderit soluta, eos quod consequuntur itaque. Nam.
---

While developing my volumetric cloud shader I came across the need for various noise patterns of specific types and qualities. There are a few good ones inside of the Volumetrics official plugin for unreal, but instead of using these I thought it could be fun to create my own.

Before this, I was generating cloud textures from shader parameters at runtime, but this was expensive and made it hard to see what was going on within the texture itself. It resulted in a lot of trial and error, changing the noise generation parameters to get a good final look. It’s definitely more effective to just sample texture assets. 

I set out to create a tool for unreal engine that would allow the user to create various noise textures, both as 2d and 3d texture assets. This would allow me to experiment with different noise parameters, resolutions and types to refine the look of my volumetric clouds. Because I was working with clouds, I initially wanted three noise types, Perlin, Worley and a combination of the two Perlin-Worley noise. I created a blueprint library in C++ that contained functions for generating tileable perlin and worley noise, then played around with different methods of combining these noise patterns to try and get results that mirrored the noise used in Horizon: Zero Dawn’s cloud rendering noise, based on a GDC cloud rendering talk I had seen. In the end I found good results from multiplying an inverted perlin noise over a worley noise pattern, and playing around with a clamp on the values of the perlin noise. This created a texture that resembled the head of a cauliflower which is ideal for use on those puffy Cumulonimbus clouds.

![thumbs1](img/noise/thumbs.jpg)

I added the ability for the user to get each channel of a texture to a different noise pattern. This meant that I could use one 3d texture for all of the cloud generation setup. Following the Horizon: Zero Dawn method, I set up the texture’s red, green and blue channels to have perlin-worley noise of increasing frequency. This would be layered like a FDM texture in the cloud shader. In the textures alpha channel I have a perlin noise, which can be used for general cloud placement. Next I made a 2d RGB texture of low resolution perlin-worley noise of increasing frequency to use for cloud edge erosion.

To make the tool more user friendly, I created an editor widget that houses all the settings for the texture. The user can set how many channels are active, and the specific noise pattern for each channel. Maybe in the future I’ll include a preview, but for now I just have a button that runs the generation and saves it to a texture asset within the project, at a location the user can set. I also included a warning to tell the user when their resolution or frequency settings would result in a texture that wouldn’t correctly tile.

![generator1](img/noise/generator.jpg)

A small but useful tool that saves me having to open Houdini by being able to generate the noise in the engine. 


![3dnoise2](img/noise/3dnoise.jpg)

*The final output of the generator*


