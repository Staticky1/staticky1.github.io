---
layout: default
modal-id: 1
date: 2014-07-18
img: cloud1.jpg
alt: image-alt
project-date: April 2014
client: Start Bootstrap
category: Unreal Engine 5, C++, Materials, Volumetric Shaders
description: Use this area of the page to describe your project. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Mollitia neque assumenda ipsam nihil, molestias magnam, recusandae quos quis inventore quisquam velit asperiores, vitae? Reprehenderit soluta, eos quod consequuntur itaque. Nam.
---

In this project, I expanded upon Unreal Engine’s default volumetric cloud system to create a custom volumetric cloud material and a dynamic weather system driven by data assets. 

Dissatisfied with the limitations of the default cloud settings, I designed a new material to intergate into the unreal volumetric cloud system from scratch, gaining extensive experience in volumetric rendering, ray casting, and ray marching, as well as optimizing performance for real-time applications.

![cloud2](img/clouds/clouds2.jpg)
![cloud5](img/clouds/clouds5.jpg)

Key features and innovations of the project include:

**Custom Cloud Material:** Developed using Unreal’s Material Graph, incorporating 3D textures for volumetric noise and using graph assets to control cloud shapes. This allows artists to modify cloud appearance easily without directly adjusting low-level material parameters.  

**Dynamic Weather System:** Driven by data assets that define cloud coverage, type, rain level, and other weather parameters. The system smoothly blends between weather states during runtime using render targets to generate masks that control transitions across the game world. 

**Realistic Visuals:** Experimented with cloud shapes, density, and lighting effects, drawing inspiration from real-world how other games achieve realistic skies.  

![cloud8](img/clouds/clouds8.jpg)

I designed the system to be efficient and scalable, with minimal performance impact on gameplay. The cost of the dynamic weather system depends on how much of the screen contains clouds:  

Dynamic weather system: ~0.5 ms mostly because of the large render targets.

Volumetric clouds: ~4 ms on average, settings tweaks can lower this at the cost of looks.

While there is still room for optimization, it's always a balance between beauty and speed and for this project I wanted beauty.


![cloud3](img/clouds/clouds3.jpg)

Through this project, I developed a strong understanding of volumetric shaders, GPU-efficient rendering techniques, and complex material workflows within Unreal Engine. Additionally, I gained practical experience in creating artist-friendly systems for procedural and data-driven environments, bridging the gap between technical programming and visual design.

![cloud7](img/clouds/clouds7.jpg)
![cloud4](img/clouds/clouds4.jpg)