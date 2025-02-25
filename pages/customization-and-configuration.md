---
title: Customization and configuration
layout: default
nav_order: 8
---
## Customization and configuration

There are lots of different customization options for making your site unique, like changing colours, header images, backgrounds, and more. As long as your changes are cosmetic, you can make customization changes in the GitHub.com interface. If you need to make any changes to your metadata file, it’s recommended that you do so in the local version of your repository and then push the changes to your GitHub.com version, since you’ll have to re-run all the Wax tasks to create pages, update the search index, and change derivatives.

**Table of Contents**
1. TOC
{:toc}

### Header

You can edit the formatting of the header by editing the **header.html** include. You can edit the title and navigation buttons in the header by editing settings in the **`_config.yml`** file. You can also change the aesthetics and content of the header in `_includes/header.html`. You can change the arrangement of the items in the navigation bar by editing the class settings for each element that includes 'navbar'. In line 11 of the include, for example, you can change `ul class='nav navbar-nav ml-auto justify-content-center'` to `ul class='nav navbar-nav ml-auto justify-content-end` to make all of the navbar items align with the left side of the screen. For all of your options, or to write new ones, see the `_sass/wax.scss` file.

### Editing pages

You can change the contents of any page on the site. Add new pages or change what’s on a page by writing content using Markdown, adding includes, and setting up your page in the front matter. **Note that whatever permalink you specify in the front matter for your page is the link you’ll have to use in the navigation section of the `_config.yml file`.** For example, if I want my page to be reached at [myusername.github.io/myreponame/crabapple](http://myusername.github.io/myreponame/crabapple)/, I would need to make the permalink in the front matter and link in the `_config.yml` file: **‘/crabapple/’**.

To add a gallery, parallax image, or other include to your page, add a [Jekyll include tag](https://jekyllrb.com/docs/includes/) into your content. Note that each include has its own set of parameters that determine what content they display. For example, parallax_image includes need you specify an image in the include to display with parameters, e.g. `collection='qatar' pid='obj12'`. Browse the [pages in the Wax demo repository](https://github.com/minicomp/wax) to get a sense of what parameters various includes take.

Note that the home/front page of your site is the **`index.md`** file, which isn’t located in the pages folder.

### Layouts
Wax five layouts for you to use and/or expand on: `wax/default.html`, `wax/page.html`, `wax/exhibit.html`, `wax/collection_item.html`, and `wax/reuse_page.html.`

You can tell a page to use a layout by adding it to the page’s front-matter, for example:
```
_exhibits/my-exhibit.md

---
title: 'My Exhibit'
layout: wax/exhibit
---
```

Or you can make your own layout file that inherits from a Wax layout, for example the qatar_item.html layout which inherits from generic_collection_item.html:
```
_layouts/qatar_item.html

---
layout: generic_collection_item.html
image_viewer: 'openseadragon'
pagination: true
meta:
  - label: 'Object Label'
    value: page.label
  - label: 'Artist'
    value: page.artist
  - label: 'Object Type'
    value: page.object_type
  - label: 'Location'
    value: page.location
  - label: 'Current Location'
    value: page.current_location
  - label: 'Date'
    value: page.\_date
  - label: 'Source'
    value: page.source
---
```
### Title, collections and exhibits, and navigation

If you’d like to change the main title of the project or the organization of pages, collections, or exhibits, including the site’s navigation bar, you can do all of this in the **`_config.yml`** file. These edits are pretty straightforward: simply delete the content that’s within each pair of single quotes ‘ ’ in a line and replace it with your own. Remember to maintain the indenting that you see on the template for this page.

### Footer

You can edit the links and logo that appear in the footer in the `_config.yml` file. You can edit the formatting of the footer by editing the footer.html include.

### Header

You can edit the formatting of the header by editing the **header.html** include. To edit the justification of the navigation bar, change line 12 of the **header.html** include. You can edit the title and navigation buttons in the header by editing settings in the **`_config.yml`** file. 

### Colors, fonts, and image dimensions

You can edit the default text colors, background colors, and fonts for your site in the **`styles.scss`** file. As with the `_config.yml` file, simply delete the content that’s in each line and replace it with your own. If you’d like to use a Google Font, see the [Google Fonts API Documentation](https://developers.google.com/fonts/docs/getting_started) for how to get the right URL for the styles.scss file.

You can also edit the dimensions of thumbnail images and viewers in the `assets/styles.scss` file.

### Editing table
This editing table is incomplete and will be continously updated as needed. If you have an element you're looking to edit that's not in this table, reach out to have it added:
<br>

| Visual element | File |
| ----- | ----- |
| Body font | `styles.scss` |
| Heading font | `styles.scss` |
| Logo | `styles.scss`; `_config.yml` |
| Image size | `styles.scss` |
| Colors (text, background, accents) | `styles.scss` |
| Viewport/image viewer size | `styles.scss` |
| Text & image margins | `styles.scss` |
| Footer height | `styles.scss` |
| Footer logo and links | `_config.yml` |
| Site title | `_config.yml` |
| Site description | `_config.yml` |
| Site URL & base URL | `_config.yml` |
| Default item image | `_config.yml` |
| Collections (including default item page layout, collection metadata file, and image folder) | `_config.yml` |
| Search fields | `_config.ym` |
| Navigation bar/menu items and links | `_config.yml`|
| Navbar justification | `header/html` |
| Front page banner image | `index.md` |
| Collection metadata | `_data` |
| Collection images | `_data/raw_images` |
