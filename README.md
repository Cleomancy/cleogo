# Glorious Hugo Theme

The Hugo theme I use for my blog, [CLEOMANCY(dot)BLOG](https://blog.cleomancy.com/).
Focused on simplicity and accessibility.
Based on [lugo](https://github.com/lukeSmithxyz/lugo).

## Install

```sh
hugo new site urSite
cd urSite
git clone https://github.com/Cleomancy/cleogo themes/cleogo
echo "theme = 'cleogo'" >> hugo.toml
cp themes/lugo/static/style.css static/
```
In urSite/static/ you can edit the copied style.css to overwrite the theme's CSS. You should also copy config.toml into hugo.toml to edit this theme's settings.

## Features

- Makes one RSS feed for the entire site at `/index.xml`
- `nextprev.html` adds links to the Next and Previous articles to the bottom of a page.
- `taglist.html` links all tags an article is tagged to for related content.
- XHTML MIME type added.
- Goldmark support for XHTML implemented.
- If you prefer HTML, minify options are implemented as well.

## Specs

I documented my process [here](https://cleomancy.github.io/hugo/index.xhtml) if you want to read more.
