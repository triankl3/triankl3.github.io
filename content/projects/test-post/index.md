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
{{% section-column title="Section column title" side="center" %}}

The header section is customized using frontmatter. Other than the basics available on screen, an image is required for the thumbnail and background. Colors are extracted and applied to elements, or you can define them manually. Also instead of the rotating cube you can specify a 3D model to be displayed.

There might be other markdown elements which are *technically supported*, but are not here. This means the blog is not accounting for them and you should avoid using them with this theme. It is mandatory to use the section shortcodes. They are there to assist in creating unique layouts for each post. View the markdown file in your editor to see more usage examples and syntax. VSCode snippets are also available to make it easier to create new sections. This was and still is a paragraph of text.

{{< img src="exampleimg1.webp" alt="This is alt text. It is only supported on single images outside of a gallery." >}}

Below you can see a splash section which simply showcases an image in full width.

{{% /section-column %}}

<!-- Splash supports setting an image and applying CSS filters directly on them -->
{{< section-splash src="exampleimg1.webp">}}

<!-- Jumbo supports setting it's text, alongisde the usual background options -->
{{< section-jumbo text="This is a huge jumbo text! Thank you for reading." background_color="#A500FF" color="#00FFA5" >}}

{{% section-column title="Model Viewer" side="center" %}}

Aenean elementum fringilla augue vitae lobortis. Fusce tellus ligula, finibus vel interdum vel, semper id arcu. Sed orci neque, fringilla et condimentum eget, tincidunt nec sapien. Sed mi tortor, feugiat id nibh quis, imperdiet mollis sem. Phasellus semper metus sed tortor suscipit, vel ultricies purus suscipit.

**A 3D model preview is also available with full controls and support for gltf and glb files.**

{{< model alt="Default suzanne monkey model from the Blender software." src="rat.glb" >}}

Below as you can see, similarly to the section-splash, we have section-splash-model which showcases a 3D model.

{{% /section-column %}}

{{< section-splash-model src="rat.glb" >}}

{{% section-column title="More examples" side="center" background_img="exampleimg1.webp" %}}

**This section has a background image set. It adjusts the opacity of the entire section and allows for a background image to be seen underneath.** Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum vitae gravida erat. Phasellus sodales nibh auctor porta venenatis. Sed massa dolor, blandit a leo eget, egestas mattis sapien. Vestibulum viverra enim eget luctus dapibus. Cras et tellus non dolor elementum luctus eget cursus dolor. Cras lectus enim, viverra quis turpis sit amet, cursus consectetur sapien.

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

Please keep in mind for legibility, design and readability reasons code blocks will retain the default black background and white text. Generally they should be used sparingly, but if need be they're available!

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

{{% /section-column %}}

{{% section-column title="White column section" side="left" background_color="white" %}}

You can also use the background attribute of the section-column shortcode to set a background color. You can set a hex code or use black/white as a shorthand. You can leave empty for black as it is default. When using the white shorthand it also automatically sets the text color to black. Otherwise you can use the color attribute to set text color manually.

Also, this column is sided on the left side. Each column can be set to left/center/right using the side attribute.

# Heading level one
## Heading level two
### Heading level three

To create lines with breaks simply leave two spaces after a line.  
We **love using bold** text sometimes. Using *italic* is also really interesting. But together they are ***fabulous***!  
~~The world is flat.~~ We now know that the world is round.

> Jerry can be a jerk sometimes, Dorothy says after following him around for 5 minutes.

Have you ever used [github](https://github.com/)?  
Links are also automagically created like this https://example.com, but that's ugly unless on purpose.

{{% /section-column %}}

<!-- Two column sections are wrapped in the section-two-column shortcode, with the left and right inside -->
<!-- You can apply the same properties as with section-column to the parent section-two-column shortcode -->
{{< section-two-column title="This is a two column section" >}}
{{% section-two-column-left %}}

Two column sections allow for content to flow on right and left in two columns with 2/3 width ratio.

{{< video src="examplevid1.mp4" >}}

Nunc suscipit, augue vel viverra cursus, sapien nulla tempus dui, vehicula euismod metus nisl vitae leo. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae; Quisque nec porta risus. Sed tincidunt dapibus purus, pretium aliquam lacus tristique ac. Nunc maximus egestas enim ac tincidunt. Morbi bibendum maximus orci sed elementum. Donec vitae purus lacus.

{{% /section-two-column-left %}}
{{% section-two-column-right %}}

This right column contains this text(paragraph) and the image gallery below.

<!-- Markdown is set to unsafe rendering, adding shortcodes in markdown text is supported -->
{{< gallery >}} <!-- You can use the gallery to support showing a grid of images in a gallery format -->

{{< img src="exampleimg1.webp" >}}
{{< img src="exampleimg2.webp" >}}
{{< img src="exampleimg2.webp" >}}
{{< img src="exampleimg1.webp" >}}

{{< /gallery >}}

{{% /section-two-column-right %}}
{{< /section-two-column >}}