---
draft: false
title: "Procedural Cave Generation"
date: 2024-01-25
description: "Procedural cave generation in Roblox using 3D Perlin noise and a custom object placement algorithm."
tags: ["roblox", "lua", "level-design", "programming"]
image: "final1.png"
color: ["#1174d7", "#34c045"]
---

{{% section-column title="The origin" side="center" %}}

**Currently available as an MIT Licensed open-source library for Roblox**, the project features a procedural cave generation system using 3D Perlin noise and a custom object placement algorithm. The full source code is available on [GitHub](https://github.com/triankl3/genesis) with a playable and editable demo place on [Roblox](https://www.roblox.com/games/15529154687/Genesis-Demo).

The system has seen many revisions, and was originally created for the now discontinued FPS game CASHMINER. It was used to generate the the destructible environments in which players would fight. For more information about the game and it's development process you can read: [The foundation of an FPS game in Roblox](/projects/the-foundation-of-an-fps-game-in-roblox).

This system grew organically over a few years as new requirements were added to the project. Nonetheless, the core goals of the system stayed the same:
1. Procedurally generate cave environments
2. Fill those cave environments with objects
3. Generate decently large maps under 10-15 seconds
4. The environment should be completely destructible
5. Keep the system highly configurable
6. Make sure the result is deterministic from a single seed with the same configuration

{{% /section-column %}}

{{< section-splash src="final10.jpg" >}}

{{% section-column title="3D Perlin" side="center" background_img="terrain1.png" %}}

**Luckily Roblox has built-in voxel Terrain**. It is perfect for this kind of application and also it is completely editable at runtime which means we can generate, edit and destroy it on the fly. However, we need to generate the terrain first. I won't be going over the specific implementation, since there are much better sources for learning about Perlin noise and the source is availble for anyone interested.

In summary, we go over every position in the map and sample the result of perlin noise at that X, Y, Z position. We use those values determine the density of that point. If it surpasses a certain threshold we set the voxel at that position be solid, otherwise we leave it empty.

{{< gallery >}}

{{< img src="terrain1.png" >}}
{{< img src="terrain2.png" >}}
{{< img src="terrain4.png" >}}
{{< img src="terrain3.png" >}}

{{< /gallery >}}

We also multiply the final result of the density based on the distance from the center of the level and also apply another larger noise which makes the map have a distinct shape instead of being a sphere. Many other tweakable properties go in here which allow us to have not only visual variety, but also impact gameplay and movement based on the complexity of the cave.

{{< img src="terrain5.png" >}}

{{% /section-column %}}

{{% section-column title="Materials" side="center" %}}

**This looks very boring**. It's time to some variety to the map. We determine which material to generate based on the results of an additional perlin noise or simply by random chance. Also certain materials such as the grass have their position determined not only based on noise, but also based on which surfaces they can appear, in this case the floor of the cave.

**Recently the engine has finally had an update which added capability to customize the texture of terrain materials.** This allowed me to create flat colored versions of the existing materials to better fit the low-poly aesthetic of the game.

The color of the materials, their chances for generating and their texture are all highly configurable.

{{< gallery >}}

{{< img src="material1.png" >}}
{{< img src="material2.png" >}}

{{< /gallery >}}

{{% /section-column %}}

{{< section-splash src="final11.jpg" >}}

{{< section-two-column title="Object Placement" background_img="final4.png">}}
{{% section-two-column-left %}}

Object generation is the most complex and unique problem that I had to solve in this project. The goal was to generate a large amount of objects in a short amount of time, while also making sure that they are placed in a way that makes sense and is visually appealing.

Due to the fact that Roblox is a highly sandboxed engine and we don't get direct access to the way the voxel Terrain is constructed, I could not use the same approach most would when generating objects on a mesh. Instead, I had to come up with extra checks to determine which surfaces the objects can and will be placed on.

1. When generating each terrain voxel determine if there has been a difference in occupancy compared to the previous `X, Y, Z` voxels.
2. If so cache that difference and position to use as a *probe*.
3. Go over each cached *probe* and use raycasts to determine the direction of the terrain change.
4. Turn those *probes* into valid *object points* which are snapped to the terrain and categorized by material and floor, wall or ceiling.
5. Construct *object prefabs* based on assets the specified configuration.
6. Clone and place *object prefabs* on the determined valid *object points*, while also making sure objects don't overlap and respect the minimum distance between eachother.

Both the generation of objects and preparation of prefabs features a quite robust config allowing the user to modify built-in properties of Roblox instances per object, but also to randomize the rotation and the way the object is placed on the terrain. It also includes helpers for adding lighting and sound to objects.

**You also might notice that the lighting looks much better now**. The lighting is available in the demo source code, however it is not a part of the library itself. I left that up to the user to implement, since it is highly dependent on the game and the art style.

{{% /section-two-column-left %}}
{{% section-two-column-right %}}

{{< gallery >}}

{{< img src="final1.png" >}}
{{< img src="final2.png" >}}
{{< img src="final3.jpg" >}}
{{< img src="final4.png" >}}

{{< /gallery >}}

{{% /section-two-column-right %}}
{{< /section-two-column >}}

{{% section-column title="Genesis" side="center" background_img="final9.png" %}}

The final project has been wrapped into the Genesis library, because I might also release other generation types under the same project such as island generation. I highly encourage you to check out the [GitHub repository](https://github.com/triankl3/genesis) as this was a gross oversimplification of the project and there are many more features and options available. Also, the [demo](https://www.roblox.com/games/15529154687/Genesis-Demo) is quite fun and generates interesting results relatively quickly, give it a shot!

**You might of noticed that one of the key demands of the system is missing.** Destruction was implemented in the game, however it is not available in the library as it was highly specific to the game and is out of scope as it features character/player systems. It shouldn't be a bother to implement if you see a need for it though, as the final result is a voxel terrain which can be edited at runtime and the objects are nothing but instances you can destroy and manipulate.

**I'll leave you with some beautiful screenshots of the final result.**

{{< img src="final9.png" >}}

{{< gallery >}}

{{< img src="final5.png" >}}
{{< img src="final6.png" >}}
{{< img src="final7.png" >}}
{{< img src="final8.png" >}}

{{< /gallery >}}

{{% /section-column %}}