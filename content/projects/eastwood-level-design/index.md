---
draft: false
title: "Eastwood Level Design"
date: 2020-01-06
description: "Level design for a Source Engine/Garry's Mod map based on real world heightmap data."
tags: ["source-engine", "level-design"]
image: "house.webp"
---

{{% section-column title="Heightmap based terrain" side="center" background="white" %}}

The map was originally ordered as a freelance commission by a client, a vast landscape featuring a military base and city. Terrain is usually created using displacement maps in Source Engine, a grid of points which can be manipulated in 3D with texture blending to create uneven surfaces. However, due to the crude nature of the tools available in the editor it is quite difficult to achieve realistic results. [DispGen by Cannonfodder](https://developer.valvesoftware.com/wiki/DispGen) allowed me to generate a displacement map from a standard heightmap image, and during a roadtrip we took a coffee break at the [Zlatar Lake](https://maps.app.goo.gl/UFbgGP3kYeM2PDzZ9) where I realized the landscape would fit the commission.

{{< gallery >}}

{{< img src="heightmap-reference.webp" >}}
{{< img src="heightmap1.webp" >}}
{{< img src="heightmap2.webp" >}}
{{< img src="heightmap-textured.webp" >}}

{{< /gallery >}}

It is largely downscaled in reality and edited to fit better with the demands of the project, but it served a great base for the final terrain. After some fighting with the tools I managed to succesfully import the terrain and applied textures to it. Displacement maps also allow you to blend the transition between two materials. But to allow for multiple materials three blends are used allowing for the usage of grass, sand, gravel and dirt textures which were manually painted on the terrain.

{{% /section-column %}}

{{< section-splash img="skyline1.webp" filter="">}}

{{% section-column title="Nature strikes" side="center" background="" %}}

The next step was a tedious one, but rewarding. Each tree, bush and prop had to be manually copied, positioned and rotated to fit the terrain. Unfortunately, Hammer editor at the time did not have any splatting/painting tools for props. A custom grass texture was used with extra dense and detailed blades and flowers for the fields to pop.

{{< gallery >}}

{{< img src="forest1.webp" >}}
{{< img src="forest2.webp" >}}
{{< img src="forest3.webp" >}}
{{< img src="forest4.webp" >}}
{{< img src="plains1.webp" >}}
{{< img src="plains2.webp" >}}

{{< /gallery >}}

{{% /section-column %}}

{{% section-column title="Beachside" side="center" background="" %}}

The beach is decorated with reeds and logs, a fishing hut and hunting tower, with a raised road alongside the lake edge.

{{< gallery >}}

{{< img src="beach1.webp" >}}
{{< img src="beach2.webp" >}}
{{< img src="beach4.webp" >}}
{{< img src="beach3.webp" >}}
{{< img src="bridge1.webp" >}}
{{< img src="bridge2.webp" >}}

{{< /gallery >}}

{{% /section-column %}}

{{< section-splash img="house.webp" filter="">}}

{{% section-column title="Buildings" side="center" background="" %}}

The map is populated by some houses, an abandoned and desolate building, a few additional shacks and the military base.

{{< gallery >}}

{{< img src="ruins.webp" >}}
{{< img src="shack.webp" >}}
{{< img src="military1.webp" >}}
{{< img src="military2.webp" >}}

{{< /gallery >}}

{{% /section-column %}}

{{% section-column title="Roads" side="center" background="" %}}

All of this also had to be connected by some roads, which are also created from displacements and decals for blending to allow for their curved and slanted look.

{{< gallery >}}

{{< img src="roads1.webp" >}}
{{< img src="roads2.webp" >}}

{{< /gallery >}}

{{% /section-column %}}

{{< section-splash img="skyline2.webp" filter="">}}

{{% section-column title="The elusive city" side="center" background="" %}}

Unfortunately, the project was cancelled halfway through to completion and the area left for the city remained empty. However, the rest of the map was almost fully finished, excluding some buildings and a skybox to make the terrain seamless.

In general this project pushed the limits of Source Engine once again, with the map taking up the maximum possible size allowed by the game.

{{% /section-column %}}