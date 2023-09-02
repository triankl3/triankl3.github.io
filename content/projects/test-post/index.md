---
draft: false
title: "The biography of a test post"
date: 2023-08-07T18:54:11+02:00
description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Mollitia tempore recusandae aperiam rerum ipsa accusantium reiciendis doloremque voluptas, officia dolorem et expedita quaerat nam explicabo non iure? Cupiditate, ea nulla?"
tags: ["test", "post"]
image: "featured1.webp"
---

# First chapter title

There might be other markdown elements which are *technically supported*, but are not here. This means the blog is not accounting for them and you should avoid using them with this theme. There are a bunch of shortcodes which can be used to create interesting layouts in your blogpost, use them wisely. This is a paragraph.

# Heading level one
## Heading level two
### Heading level three
#### Heading level four
##### Heading level five
###### Heading level six

To create lines with breaks simply leave two spaces after a line.  
We **love using bold** text sometimes. Using *italic* is also really interesting. But together they are ***fabulous***!  
~~The world is flat.~~ We now know that the world is round.

> Jerry can be a jerk sometimes, Dorothy says after following him around for 5 minutes.

Have you ever used [github](https://github.com/)?  
Links are also automagically created like this https://example.com.

Emoji's work :skull:.

Here's a simple footnote,[^1] and here's a another one.[^textnote]

1. First item
2. Second item
3. Third item
    1. First indented item
    2. Second indented item
4. Fourth item 
    - An unordered indented item
    - We can mix and match
        - And go even deeper :moai:

[^1]: This is the first footnote.

[^textnote]: This is the other footnote.

| Syntax      | Description | Test Text     |
| :---        |    :----:   |          ---: |
| Header      | Title       | Here's this   |
| Paragraph   | Text        | And more      |

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

{{< img src="background.webp" alt="This is how alt-text / figure captions look apparently." >}}

{% include youtube.html id="iUtnZpzkbG8" %}

{% include video.html path="/assets/vid/example.mp4" %}