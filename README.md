# Glorious Hugo Theme

The Hugo theme I use for my blog, [BLOG dot CLEOMANCY](https://blog.cleomancy.com/).
Focused on simplicity and accessibility.
Based on [lugo](https://github.com/lukeSmithxyz/lugo).

## Install

```sh
hugo new site urSite
cd urSite
git clone https://github.com/Cleomancy/cleogo themes/cleogo
echo "theme = 'cleogo'" >> hugo.toml
cp themes/cleogo/static/style.css static/
cp themes/cleogo/archetypes/default.md archetypes/default.md
```
In urSite/static/ you can edit the copied style.css to overwrite the theme's CSS. You should also copy config.toml into hugo.toml to edit this theme's settings.

## Features

- Shows a 'Recent Posts' list with their summary and word count.
- Same for a specific tag page, shows the latest three posts with summary, then a full list of every posts.
- Makes one RSS feed for the entire site at `/index.xml`.
- `nextprev.html` adds links to the Next and Previous articles to the bottom of a page.
- `taglist.html` links all tags an article is tagged to for related content.
- XHTML MIME type added.
- Goldmark support for XHTML implemented.
- If you prefer HTML, minify options are implemented as well.
- `Sitemap.html` generates a sitemap for users.
- Toggleable Site subtitle + per page subtitles.

## Sitemap.html

The sitemap uses another layout, you must create a sitemap.md file in the 'content' folder:
```sh
hugo new sitemap.md
```
and make sure its archetype at least contains the following lines:

```sitemap.md
+++
layout = 'sitemap'
title = 'Sitemap'
type = 'else'
+++
```

No need to add any content to sitemap.md after those lines, in fact you shouldn't, it will not be displayed anyway.

## Specs

I documented my process [here](https://blog.cleomancy.com/hugo/) if you want to read more.
