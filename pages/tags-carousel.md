---
title: Tags
layout: page
nav_order: 2
parent: WaxBuilder
---

WaxBuilder includes tags in two places: the Browse page (at the bottom) and the Timeline page (at the top). These tags are populated based on the tTags field in your metadata file. If you click on a tag, it will populate a basic gallery layout of all the items that have that tag.
<hr class="solid">
<img src="https://kam535.github.io/wax-documentation/images/tags-timeline.png" alt="screenshot of the tags above the Timeline page">
<i>The tags above the timeline page</i>
<br>
<br>
<br>
<hr class="solid">
<img src="https://kam535.github.io/wax-documentation/images/tags-browse.png" alt="screenshot of the tags at the bottom of the Browse page">
<i>The tags above the timeline page</i>
<br>
<hr class="solid">

## Timeline tags
If you want to change what field the tags are populated from, you can specify this for the Timeline in the `_layouts/tags.html` file by replacing any instance of 'tTags' with your custom field. On the Timeline page, the tags are embedded on the page.
<br>
Timeline tags are managed by the following files:
* `_includes/tag-carousel.html`
* `tags.md`
* `assets/javascript/tag-owl.js`
* `_layouts/tags.html`

## Browse tags
You can change what field are populated on the Browse page by specifying your custom fields in the `tag-carousel.html` include in the `browse.md` file. On the Browse page, the tags are populated using an include: `_includes/tag-carousel.html`
<br>
Browse tags are managed by the following files:
* `_includes/tag-carousel.html`
* `tags.md`
* `browse.md`
* `assets/javascript/tag-owl.js`
* `_layouts/tags.html`
