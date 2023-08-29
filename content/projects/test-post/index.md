---
draft: false
title: "Test Post"
date: 2023-08-07T18:54:11+02:00
description: "Hello world this is a test post description."
tags: ["test", "post"]
image: "featured2.webp"
---

# First chapter title

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum. This is a paragraph.

# Heading level 1
## Heading level 2
### Heading level 3
#### Heading level 4
##### Heading level 5
###### Heading level 6

To create lines with breaks simply add leave two spaces after a line.  
We love using **bold** text sometimes.  
Using *italic* is also really interesting.  
But both are ***amazing***!  
~~The world is flat.~~ We now know that the world is round.

> Jerry can be a jerk sometimes, Dorothy says after following him around for 5 minutes.

Have you ever used [github](https://github.com/)?  
Links are also automagically created like this https://example.com.

Emoji's work :skull:

1. First item
2. Second item
3. Third item
4. Fourth item 

- [x] Write the press release
- [ ] Update the website
- [ ] Contact the media

1. First item
2. Second item
3. Third item
    1. First indented item
    2. Second indented item
    - An unordered indented item
    - We can mix and match
        - And go even deeper
4. Fourth item 

- Milk
- Eggs
- Mushroom stew
- Long truck 

Here's a simple footnote,[^1] and here's a longer one.[^bignote]

[^1]: This is the first footnote.

[^bignote]: Here's one with multiple paragraphs and code.

---

| Syntax      | Description | Test Text     |
| :---        |    :----:   |          ---: |
| Header      | Title       | Here's this   |
| Paragraph   | Text        | And more      |

In your command prompt you should type: `bundle exec jekyll serve`.

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

{{< img src="background.webp" alt="This is how alt-text / figure captions looks apparently." >}}

{% include youtube.html id="iUtnZpzkbG8" %}

{% include video.html path="/assets/vid/example.mp4" %}