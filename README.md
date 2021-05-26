# Hugo Apéro

<!-- Markdown snippet -->
[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/hugo-apero/iyo-apero)

[![Netlify Status](https://api.netlify.com/api/v1/badges/dfa8a8fa-cca0-4917-aae5-27d89527b7ff/deploy-status)](https://app.netlify.com/sites/silly-babbage-223d45/deploys)


# _Hugo Apéro_ - a personal website theme made for Hugo by [RStudio](https://rstudio.com/). 

Based on [Blogophonic](https://github.com/formspree/blogophonic-hugo) by [Formspree](https://formspree.io).

A modern, beautiful, and easily configurable theme for Hugo websites. It offers more than a blog, with flexible custom layouts that help you introduce yourself online.

**See the demo site [here](https://hugo-apero.netlify.com)**

**Read the docs [here](https://hugo-apero-docs.netlify.com)**

![screenshot](static/img/screenshot.png)

## Three reasons to use Apéro

1. **Apéro is thoughtfully crafted** with features a personal website _should have_: a proper "about" page; multiple layouts - including one with a sidebar; custom sidebar text with a sticky ad container; option to hide byline, dateline, and thumbnail images.

2. **Good looks are baked in** - use a built-in color theme and choose your fonts. You can have a distinct (in a good way!) site without fannying around with any CSS or font files. Plus everything **also** looks good on mobile, thanks to the responsive Tachyons CSS framework.

3. **Batteries included** - all of these just work "out of the box": social links (Font Awesome & Academicons); social sharing images and metadata; featured thumbnail images (with special support for hexagon shapes); syntax highlighting (via Chroma); commenting (via utterances); contact form (via Formspree). 

## Usage

To use it:

```r
blogdown::new_site(theme = "hugo-apero/hugo-apero")
```

Then you can edit or discard the pages under `content`, and change things in the `config.toml` file.

## Site configuration

The following site configuration options are found in the `config.toml` file at the root of this Hugo site.

### Font options

You have three options for customizing fonts:

+ Use [embedded fonts](https://hugo-apero-docs.netlify.app/blog/fonts/#embedded-fonts),
+ Use attractive [system fonts](https://hugo-apero-docs.netlify.app/blog/fonts/#use-attractive-system-fonts), or
+ Use fully [custom fonts](https://hugo-apero-docs.netlify.app/blog/fonts/#use-a-custom-font).

Find this section in your `config.toml` file and go to town:

```toml  
[params]
  # use an embedded font
  customtextFontFamily = "Commissioner"
  customheadingFontFamily = "Fraunces"
  # or choose a system font stack
  textFontFamily = "sans-serif"
  headingFontFamily = "serif"
```

Read the full docs here: https://hugo-apero-docs.netlify.app/blog/fonts/

### Color themes

You have three options for customizing colors:

+ Use a [color theme](https://hugo-apero-docs.netlify.app/blog/color-themes/#use-a-color-theme),
+ Use [Tachyons colors](https://hugo-apero-docs.netlify.app/blog/color-themes/#use-tachyons-named-colors), or
+ Bring your own [hex codes](https://hugo-apero-docs.netlify.app/blog/color-themes/#bring-your-own-hex-codes).

Find this section in your `config.toml` file and color away:

```toml
[params]
  # use a built-in color theme
  # one of: forest / grayscale / peach / plum /
  #         poppy / sky / violet / water
  theme = "peach"
  
  # or, leave theme empty & make your own palette
  # see docs at https://hugo-apero.netlify.app/blog/color-themes/
  # the custom scss file must be in the assets/ folder
  # add the filename name here, without extension
  # to use hex colors instead of named tachyons colors, include "hex" in filename
  custom_theme = "hex-colors" 
```

Read the full docs here: https://hugo-apero-docs.netlify.app/blog/color-themes/

### Social icons

You can use both Font Awesome and Academicons to link to your social accounts.

Find this section in your `config.toml` file and link all the things:

```toml
[params]
# show/hide social icons in site header/footer
socialInHeader = false
socialInFooter = false
  [[params.social]]
      icon      = "github" # icon name without the 'fa-'
      icon_pack = "fab"
      url       = "https://github.com/apreshill/apero"
  [[params.social]] <!--lather, rinse, repeat-->
```

Read the full docs here: https://hugo-apero-docs.netlify.app/blog/social/

## Page configuration

Hugo allows you to use a page's front matter (written in yaml, toml, or json) to keep metadata attached to markdown files. The motto in Hugo is "everything is a page." The following page configuration options are found in the front matter of a Hugo Apéro site.

### Section configuration

There are two sets of front matter for each content section. One set is for the section itself (`/blog/_index.md`), and the other for each page within a section, which consist of front matter plus content (`/blog/my-blog-post/index.md`). 

Apéro provides unique layouts for three main content sections:

+ blogs,
+ projects, and
+ talks.

These are easy to see in your content folder structure (note the folder names are singular, not plural):

```json
content/
├── blog/
├── project/
└── talk/
```

#### Lists of pages

For most sections, there are three listing `layout` choices: 

+ `list` (blogs, projects, talks)
+ `list-sidebar` (blogs, projects, talks), or 
+ `list-grid` (blogs and projects only).

We list each section pages with a title and excerpt plus a thumbnail, byline, and dateline according to your boolean choice here.

```yaml
title: A Blog That Works
description: |
  Words
  go
  here.
author: "Alison Hill"
show_post_thumbnail: true
thumbnail_left: true # for list-sidebar only
show_author_byline: true
show_post_date: true
# for listing page layout
layout: list-sidebar # list, list-sidebar, list-grid
```

Any of the layouts can be used with or without post thumbnails (seriously- they all look good and work well on mobile!). 

If you show thumbnails, the image file in each page's bundle with the word `featured` in the filename will be used as the page thumbnail in the list (like `featured.jpg` or even `mario-kart-featured.png`). The featured image will also be that page's social sharing image. 

```json
content/
├── blog
│   ├── _index.md
│   ├── my-blog-post
│   │   ├── my-featured.jpg
│   │   └── index.md
```

If your image happens to be a hex shape (like an R package hex sticker), include the word `hex` in the filename too, like `my-featured-hex.png`.

#### List sidebar content

If you choose the `list-sidebar` layout for a section, you can configure the sidebar content in the same `/section/_index.md` file.

```yaml
# for list-sidebar layout
sidebar: 
  title: A Sidebar for Your Thoughts
  description: |
    Sidebar
    thoughts
    go here.
  author: "Alison Hill"
  text_link_label: Subscribe via RSS
  text_link_url: /index.xml
  show_sidebar_adunit: true # show ad container
```

To display an image at the top of the sidebar, add an image file to the root of the content section and name the file `sidebar-listing`. 

```json
content/
├── blog
│   ├── _index.md
│   └── sidebar-listing.png
```

### Single pages

You have two options for where to place front matter for single pages. You can use the front matter of the page like `/blog/my-blog-post/index.md`, or you could use the `cascade` key in the section front matter like `/blog/_index.md`. You can set up the cascade to avoid repeating yourself, if you want to make sure to configure all pages in the same section the same way:

```yaml
# set up common front matter for all pages inside blog/
cascade:
  author: "Alison Hill"
  show_author_byline: true
  show_post_date: true
  show_comments: true # see site config to choose Disqus or Utterances
```

You can still override any of these options in the YAML front matter of an individual page- it will always trump the cascade if present.

In the front matter of a page, along with things you'd expect like title, subtitle, excerpt, and author, there are two choices for `layout`: 

+ `single` or 
+ `single-sidebar`. 

```yaml
layout: single # single or single-sidebar
```

Either of these layouts will work for any content section (blogs, projects, talks), and can even be mixed and matched within any content section. You can also add link buttons to the top of a single page in any content section (helpful for sharing external resources related to a page like a slide deck, YouTube video, GitHub repository, etc.):

```yaml
links:
- icon: door-open # icon name without the 'fa-'
  icon_pack: fas
  name: website
  url: https://allisonhorst.github.io/palmerpenguins/
- icon: github # icon name without the 'fa-'
  icon_pack: fab
  name: code
  url: https://github.com/allisonhorst/palmerpenguins/
- icon: newspaper # icon name without the 'fa-'
  icon_pack: far
  name: Blog post
  url: https://education.rstudio.com/blog/2020/07/palmerpenguins-cran/
```

For each link, pick your `icon` and `icon_pack` from the [Font Awesome](https://fontawesome.com/) [fab / fas / far] or [Academicons](https://jpswalsh.github.io/academicons/) [ai] free icon libraries. 

All external links (i.e., those that start with `http`) will open in a new tab (that is, `target="_blank"`); relative links to pages within the site will open in the same window (links relative to your site root should start with `/`; links relative to the current page should not; to link up from current directory use `../` to go up a level).

#### Page sidebar content

When you use the `single-sidebar` layout, the sidebar contents can be controlled by either the page file (`/blog/my-blog-post/index.md`) or the the section page file (`/blog/_index.md`) containing a set of front matter for that section's sidebar. In this file you can specify an image, title, description, author name (good for groups or teams), a text link and a boolean for the ad unit. 

```yaml
# set up common front matter for all pages inside blog/
cascade:
  # for single-sidebar layout
  sidebar:
    text_link_label: View recent talks
    text_link_url: /talk/
    show_sidebar_adunit: false # show ad container
```

By default, the page sidebar will use the section's `sidebar-listing` image if present. To instead use a unique page-specific sidebar image, the image file in that page's bundle with the word `sidebar` in the filename will be used in the sidebar (like `sidebar.jpg` or even `mario-kart-sidebar.png`). 

```json
content/
├── blog
│   ├── _index.md
│   ├── sidebar-listing.png
│   ├── my-blog-post
│   │   ├── my-featured-thumbnail.jpg 
│   │   ├── my-post-sidebar.jpg
│   │   └── index.md
```

If you want the sidebar image to **also** be the thumbnail image on the listing page, add the word `featured` to the filename (like `featured-sidebar.jpg` or even `mario-kart-sidebar-featured.png`). The featured image will also be that page's social sharing image. 

### Home page

Fill out the YAML in `/content/_index.md`:

```yaml
---
title: "Alison Hill"
subtitle: "Product Manager, Data Science Communication @RStudio"
description: |
  longish
  text
  here.
images:
  - img/home.jpeg
image_left: false
text_align_left: true
show_social_links: true # specify social accounts in site config
show_action_link: true
action_link: /about
action_label: "About me &rarr;"
action_type: text # text, button
type: home
---
```

Read the full docs here: https://hugo-apero-docs.netlify.app/blog/homepage/

### About page

Fill out the YAML front matter in four markdown files:

+ `/content/about/_index.md`,
+ `/content/about/header/index.md` (if you want one),
+ `/content/about/main/index.md` (the wide column), and
+ `/content/about/sidebar/index.md` (the narrow column).

To change which content sections are previewed, use `mainSections` in your `config.toml` file:

```toml
[params]
  mainSections = ["blog", "project", "talk"]
```

Read the full docs here: https://hugo-apero-docs.netlify.app/blog/about-page/


### Regular page

A regular page (not a form and not a page in a content section like blogs, projects, or talks) has a few configurations as well. There are two `layout` options: `standard` or `wide-body`, and an option to show the page title as a large headline at the top above the content.

```yaml
layout: standard # standard or wide-body
show_title_as_headline: false
```

### Contact page

This website comes with a Formspree form that's designed to work with a static website. You can use `hugo new` to create a new form in the `/form` directory or, just use the one already present in the site content.

```bash
hugo new form/contact.md
```

Your new contact page contains auto-generated front matter that defines the form name, title, date, and url, and more. Most important is the `formspree_form_id` key. Replace `your@email.here` with your form's `hashid`. You can find this on the integration page which is displayed after you create a new form. It looks like `https://formspree.io/<hashid>`.

You can also specify a description that will display below the title, choose a right or left position for the form itself via `layout`, set a preferred `submit_button_label`, and toggle a few things on or off.

```yaml
description:
layout: split-right # split-right or split-left
submit_button_label: Send
show_social_links: true
show_poweredby_formspree: true
formspree_form_id: your@email.here
```
