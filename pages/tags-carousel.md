---
title: Tags
layout: page
nav_order: 2
parent: WaxBuilder
---

WaxBuilder includes tags in two places: the Browse page (at the bottom) and the Timeline page (at the top). These tags are populated based on the tTags field in your metadata file. 

If you want to change what field the tags are populated from, you can specify this for the Timeline in the `_layouts/tags.html` file by replacing any instance of 'tTags' with your custom field. You can change what field are populated on the Browse page by specifying your custom fields in the `tag-carousel.html` include in the `browse.md` file.
