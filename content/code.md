---
title: "Shortcodes"
date: 2021-02-05T13:03:42+13:00
draft: true
type: code
---
## Preamble
This is an independent page. Independent pages aren't as simple as Jekyll, where you can create a basic HTML and link to it.
Important for creating single pages like this: set `type: <layout convention name>`. Here, the example is `content/code` and `layouts/code`, so we use `type: code`

Shortcodes are essentially plugins for Hugo. Custom shortcodes need to be created in the `layouts/shortcodes` directory.

## How-to guide

### Note: shortcodes must be used in content files, not HTML.

- Create `layouts/shortcodes`
- Add your `<shortcode-name.html>` page.
- Create your code structure in HTML
- Replace any areas that should remain changeable with Go templating.
- Include the shortcode anywhere you need it, by name. Use **{{</* myshortcode */>}}** if there's markdown to process, or  if there's none.
- Insert any parameters next to shortcode name, in order or named (another topic).

### Examples - built-in shortcodes

{{< figure src="/bhut.jpg" title="Crazy hot chillies" >}}


### Custom example:

Probably not greatly useful (hardcoded `images.yml` in the shortcode; more work than just recreating a gallery in HTML), but a fun demonstration:

- Unprocessed images are in a `resources` folder called `desert_gallery`
- Because we also want to add alt tags, we've got the paths and the alt text in a data file
- To get this data, we provide gallery with the collection name inside `images.yml` to search for
- Optionally, we can provide dimensions for resizing.

Ultimately, not very useful, but hey.

{{< gallery source="desert" dimensions="600x400" >}}