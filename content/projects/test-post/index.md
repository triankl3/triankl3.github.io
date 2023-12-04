---
draft: true
title: "The biography of a test post"
date: 2023-08-07T18:54:11+02:00
description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Mollitia tempore recusandae aperiam rerum ipsa accusantium reiciendis doloremque voluptas, officia dolorem et expedita quaerat nam explicabo non iure? Cupiditate, ea nulla?"
tags: ["project", "testpost"]
image: "exampleimg1.webp"
model: "rat.glb"
---

<!-- When available you can set a sections background with the following options: background="black(default)/white/#hexhex  " -->

<!-- Use section column to create one vertical column. Chose alignment sides with side=center(default)/left/right . -->
<!-- title="text" is available to set a huge title for the section -->
{{% section-column title="Section column title" side="center" background="" %}}

There might be other markdown elements which are *technically supported*, but are not here. This means the blog is not accounting for them and you should avoid using them with this theme. There are a bunch of shortcodes which can be used to create interesting layouts in your blogpost, view the markdown file in your editor to see more usage examples and all variations. This is a paragraph.

{{< img src="exampleimg1.webp" >}}

# Heading level one
## Heading level two
### Heading level three

To create lines with breaks simply leave two spaces after a line.  
We **love using bold** text sometimes. Using *italic* is also really interesting. But together they are ***fabulous***!  
~~The world is flat.~~ We now know that the world is round.

> Jerry can be a jerk sometimes, Dorothy says after following him around for 5 minutes.

Have you ever used [github](https://github.com/)?  
Links are also automagically created like this https://example.com.

{{< model alt="Default suzanne monkey model from the Blender software." src="rat.glb" >}}

{{% /section-column %}}

<!-- Splash supports setting an image and applying CSS filters directly on them -->
{{< section-splash img="exampleimg1.webp" filter="invert(1)">}}

<!-- Jumbo supports setting it's text, alongisde the usual background options -->
{{< section-jumbo text="This is a huge jumbo text! Thank you for reading." background="#FFA500" >}}

<!-- Two column sections are wrapped in the section-two-column shortcode, with the left and right inside -->
<!-- You can apply the same properties as with section-column to the parent section-two-column shortcode -->
{{< section-two-column title="This is a two column section" background="white" >}}
{{% section-two-column-left %}}

Lorem ipsum dolor sit amet consectetur adipisicing elit. Mollitia tempore recusandae aperiam rerum ipsa accusantium reiciendis doloremque voluptas, officia dolorem et expedita quaerat nam explicabo non iure? Cupiditate, ea nulla?

Emoji's work :skull:.

1. First item
2. Second item
3. Third item
    1. First indented item
    2. Second indented item
4. Fourth item 
    - An unordered indented item
    - We can mix and match
        - And go even deeper :moai:

{{< video src="examplevid1.mp4" >}}

{{% /section-two-column-left %}}
{{% section-two-column-right %}}

In your command prompt you should type: `npm run serve`.

```lua
--please don't take this code seriously
local module = {}

local TREE_HEIGHT_RANGE = NumberRange.new(10, 40)

--this is a really useless function, but it works!
function module.randomTreeStats()
    return math.random(TREE_HEIGHT_RANGE.Min, TREE_HEIGHT_RANGE.Max)
end

--here is an example of a very long line
function module.boxRegion3(pos, size)
    return Region3.new(pos - Vector3.new(size.X / 2, size.Y / 2, size.Z / 2), pos + Vector3.new(size.X / 2, size.Y / 2, size.Z / 2))
end

return module
```

<!-- Markdown is set to unsafe rendering, adding shortcodes in markdown text is supported -->
{{< gallery >}} <!-- You can use the gallery to support showing a grid of images in a gallery format -->

{{< img src="exampleimg1.webp" >}}
{{< img src="exampleimg2.webp" >}}
{{< img src="exampleimg1.webp" >}}
{{< img src="exampleimg1.webp" >}}
{{< img src="exampleimg2.webp" >}}
{{< img src="exampleimg2.webp" >}}

{{< /gallery >}}

{{% /section-two-column-right %}}
{{< /section-two-column >}}