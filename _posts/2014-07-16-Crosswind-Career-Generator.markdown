---
layout: default
modal-id: 3
date: 2014-07-16
img: Crosswind1.jpg
alt: image-alt
project-date: April 2014
client: Start Bootstrap
category: Software Development
description: Dynamic Career Generator for IL-2 Sturmovik Battle of Stalingrad
---
For this project, I developed a comprehensive career generator for IL-2 Sturmovik: Battle of Stalingrad, called Crosswind. The program would run separately to the flight simulator but would have access to the game files. It would allow players to create a pilot in a specific squadron and experience the campaigns featured in the game, aligned with historical developments, frontline movements, and key battles.

The program simulates multiple squadrons operating in a theater, tracking each pilot’s progress and automatically generating missions as the player advances through the campaign day by day. When a player is assigned a mission, the program creates a corresponding mission file that can be played directly in IL-2. After completing the mission, the program parses the game logs to determine the outcome, updating the player’s statistics and the performance of all AI pilots involved. AI pilots would be assigned to squadrons and their experience would be translated into their in game skill. Pilots would increase in skill after successful missions. Aircraft damage, pilot injury and loss were all tracked.

![Crosswind5](img/crosswind/Crosswind5.jpg)

To enhance the user experience, the program uses Vulkan to render images of aircraft, squadrons, and frontlines. This provides a fast, hardware-accelerated visual representation of the simulated world, allowing players to quickly understand squadron positions, mission targets, and campaign progress at a glance. The Vulkan integration required careful management of GPU resources and real-time rendering pipelines while keeping the UI responsive and clean.

This was my first attempt at developing a large-scale Windows application. I placed strong emphasis on designing a clean and intuitive user interface, making it easy for users to interact with complex systems. The program is written in C++ and leverages XML files for all data storage, ensuring that new squadrons, missions, and pilots can be easily added or modified. The project did become cumbersome and somewhat hard to manage. I also found that programming standards mistakes that I had made earlier in the project eventually came around to bite me. 

![Crosswind3](img/crosswind/Crosswind3.jpg)

Through this project, I gained significant experience in planning and structuring a large software project, emphasizing maintainable code, modular architecture, and data-driven design. It was a valuable exercise in balancing simulation complexity with usability and in understanding the workflow of integrating an external game with a custom management tool.

![Crosswind4](img/crosswind/Crosswind4.jpg)