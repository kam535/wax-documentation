---
title: Timeline
layout: page
nav_order: 2
parent: WaxBuilder
---
# Timeline

The timeline is a feature of WaxBuilder modified from Joseph Anderson of the Fashion Institute of Technology NYC’s Digital Initiatives [museum-timeline](). To be displayed in the best way, it exists as it's own page attached to WaxBuilder, with a tags section at the top, a return to WaxBuilder button, and an interactive timeline slider that pulls from the dateStart and dateEnd fields of your metadata spreadsheet. The timeline is managed by the following files:
* `_includes/tag-carousel.html`
* `_includes/timelinehead.html`
* `_includes/timelineheader.html`
* `_layouts/timelinedefault.html`
* `_layouts/timeline.html`
* `assets/timelinejs.json`
* `assets/timelinestyles.css`
* all javascript files in the `assets/javascript` folder

## timelinehead.html
Replaces the default head (`head.html`) with a specific head for the timeline page.

## timelineheader.html
Replaces the default header (`header.html`) with a specific header for the timeline page.

## timelinedefault.html
Replaces the default layout (`default.html`) with a specific layout for the timeline page.

## timeline.html
The layout for the timeline page. Runs the actual functions to produce the timeline, including the scripts in the `assets/javascript` folder.

## Creating a timeline page
To create a timeline page, simply add a markdown file to your `_pages` directory. Set the layout to `timeline` in the Jekyll front matter. You can change which field the tags are produced from using the documentation on the [tags page]().


