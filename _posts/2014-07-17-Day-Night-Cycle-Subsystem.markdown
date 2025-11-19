---
layout: default
modal-id: 2
date: 2014-07-17
img: daynight.jpg
alt: image-alt
project-date: April 2014
client: Start Bootstrap
category: Unreal Engine 5, C++, Dynamic Lighting, Sky/Atmosphere Materials, Material Shading, Astronomical Calculations
description: DayNightCycle
---

For this project, I developed a day-night cycle subsystem in Unreal Engine that accurately simulates the positions of the sun and moon based on real-world data. Written in C++, the system allows users to set a local time as well as latitude and longitude, and the subsystem calculates and displays the correct positions and paths of the sun and moon across the sky throughout the day. I implemented my system from scratch not realising that there is already a plugin that contains many of the calculation functions.

![daynight3](img/daynight/daynight3.jpg)

This project required a deep understanding of Unreal Engine’s dynamic lighting system, atmosphere setup, and interaction with material systems. I also created a complex sky sphere material, extending the one included in the Sun position calculator plugin. The material includes:

Correct mapping of the lunar surface from a flat texture, I set it up to allow for rotation of the moon but our moon is tidally locked.

Moon terminator effect for realistic daytime shading on the moon.

Accurate moon phases that dynamically change the intensity and distribution of moonlight.

The system integrates with Unreal’s lighting pipeline to ensure that both directional light (sun and moon) and atmospheric effects respond correctly to changes in time and location. This project taught me a lot about dynamic lighting, atmosphere rendering, and material-driven environmental effects in Unreal, as well as how to combine mathematical astronomical calculations with game engine visual systems.

![daynight2](img/daynight/daynight2.jpg)
