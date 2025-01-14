---
title: Customization and configuration
layout: default
nav_order: 8
---

## Site settings
The main settings are direct from Jekyll. You can learn more through their [configuration guides](https://jekyllrb.com/docs/configuration/).

<code>

title:            'Minicomp/Wax'
description:      'Minimal Exhibitions with Jekyll'
url:              'https://minicomp.github.io'
baseurl:          '/wax'
copyright:        'Example copyright org, 2018'

</code>

## Collection settings
Wax leverages [Jekyll collections](https://jekyllrb.com/docs/step-by-step/09-collections/) for much of its functionality, therefore some of the keys below are from Jekyll while others are Wax-specific.

Below, two collections — exhibits and your-collection-name — are configured. They are made up of Markdown files in `_exhibits` and `_qatar` respectively. Exhibits contains regualr written Markdown files, so it only needs `output: true` in its config. The collection you'be been building in the last few steps is a Wax image/media collection and needs more info to be processed.

You'll need to open the `_config.yml` file and change the following:
* Replace`qatar` with your actual collection name, in all lowercase characters.
* Replace `qatar_item` with whatever you renamed the layout `qatar_item` in the `_layouts` folder to be.
* Replace `qatar.csv` with your metadata file name.
* Replace `raw_images/qatar` with the filename of your folder of item files. 

<code>

  collections:
  exhibits:
    output: true
  qatar:
    output: true
    layout: 'qatar_item'
    metadata:
      source: 'qatar.csv' # path to the metadata file within `_data`
    images:
      source: 'raw_images/qatar' # path to the directory of images within `_data`
      
</code>
