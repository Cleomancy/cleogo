# Glorious Hugo Theme

The Hugo theme I use for my blog, [CLEOMANCY sl/\sh BLOG](https://cleomancy.com/blog).
Focused on simplicity, accessibility, small size and *speed*.
A far cry but originally based on [lugo](https://github.com/lukeSmithxyz/lugo).

## Install

```sh
hugo new site urSite
cd urSite
git clone https://github.com/Cleomancy/cleogo themes/cleogo
cp themes/cleogo/config.toml hugo.toml
cp themes/cleogo/static/style.css static/
cp themes/cleogo/archetypes/default.md archetypes/default.md
```
In urSite/static/ you can edit the copied style.css to overwrite the theme's CSS. You should also copy config.toml into hugo.toml to edit this theme's settings.

## Features

- Shows a 'Recent Posts' list with their summary, read time and last modification date. (3 latest posts).
- Any content for the index page (_index.md) is displayed after the first three posts list.
- Same for a specific tag page, shows the latest three posts with summary, then a full list of every posts.
- Makes one RSS feed for the entire site at `/index.xml`.
- `nextprev.xhtml` adds links to the Next and Previous articles to the bottom of a page.
- `taglist.xhtml` links all tags an article is tagged to for related content.
- XHTML MIME type support (and default).
- Goldmark support for XHTML implemented.
- `Sitemap.xhtml` generates a sitemap for users.
- shows word count and last modifications dates at the bottom of each posts.
- Multilingual support (french is added here as an example)
- Multilingual support works with the RSS feed of course

## Sitemap.html

The sitemap uses another layout, a sitemap.md file in the 'content' folder is provided.

Its archetype contains the following:

```sitemap.md
+++
slug = 'sm'
layout = 'sitemap'
title = 'Sitemap'
type = 'sm'
+++
```

It must have a slug set to "sm" as it is the referer used in the footer menu, otherwise our sitemap would be in /sitemap/ and would conflict with Hugo's xml sitemap generation.

DO NOT add any content to sitemap.md,  it will not be displayed and will break the sitemap itself (not drastically but still).

DO NOT run the command `hugo new sitemap.md` it won't work, it's already created.