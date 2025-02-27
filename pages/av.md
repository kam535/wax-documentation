---
title: Audiovisual items
layout: page
nav_order: 5
parent: WaxBuilder
---
# AV items

For all it's strengths, Wax does not natively support audio and video items. Since the IIIF viewer for each item is an OpenSeaDragon viewer that has not been configured for this, WaxBuilder uses several different methods for making it possible to display and play audio and video items on your site. The relevant files are:
* `_layouts/av_collection_item.html`
* `_layouts/medfrag_av.html`

These two layouts mirror the native Wax layouts for `generic_collection_item.html` and `qatar.html`. `medfrag` is simply a shortened name for the sample collection in WaxBuilder. The difference is that the av layout uses the `format` field of your metadata spreadsheet to determine whether to use an audio player, IIIF audio player, or iframe (for video) to display and play your video or audio object. You must specify either: iiif-audio, audio, or video in a `format` field in your metadata spreadsheet. If you're using IIIF audio, you'll have to specify a `manifest` field with the URL to your manifest in your metadata spreadsheet. If you're using regular audio or video, you'll have to specify a `filename` field with the URL to your audio or video in your metadata spreadsheet. You can upload an MP3 or video file to your GitHub repository and use a relative link as well.

## Creating an audio/video item
There are two things you must do to create an audio/video item: 
1. Add the `format` and appropriate `filename` or `manifest` fields in your metadata spreadsheet before you run wax tasks.
2. Add your links to the metadata spreadsheet in the above fields.
3. Edit your individual object pages and metadata sheet with the av layout (e.g. `medfrag_av`) after running wax tasks.
Your audio/video objects should then appear just like a normal image or IIIF object on the browse page, map, etc.

## The iiif-audio format
The iiif-audio format exists to support the IIIF Cookbook recipe, Audio Presentation with Accompanying Image, which displays an image while audio plays in a Clover viewer. If you'd like to create this type of manifest, please see the [IIIF Cookbook recipe](https://iiif.io/api/cookbook/recipe/0014-accompanyingcanvas/). [Object 24 of the sample site](https://kam535.github.io/waxbuilder/medievalfragments/obj24/) is a good example of this type of manifest.

**This feature is the most "in-progress" feature of WaxBuilder.** I am currently in the process of simplifying the paths to the players, as well as making it so that you won't have to constantly edit things in the individual page and CSV file post-wax tasks in order to get these layouts to work. Stay tuned for updates.
