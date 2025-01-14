---
title: Configuring collections settings
layout: default
nav_order: 2
parent: Setting up your site
---
1. TOC
{:toc}

## Site settings
The main settings are direct from Jekyll. You can learn more through their [configuration guides](https://jekyllrb.com/docs/configuration/).



```
title:            'Minicomp/Wax'
description:      'Minimal Exhibitions with Jekyll'
url:              'https://minicomp.github.io'
baseurl:          '/wax'
copyright:        'Example copyright org, 2018'

```


## Collection settings
Wax leverages [Jekyll collections](https://jekyllrb.com/docs/step-by-step/09-collections/) for much of its functionality, therefore some of the keys below are from Jekyll while others are Wax-specific.

Below, two collections — exhibits and your-collection-name — are configured. They are made up of Markdown files in `_exhibits` and `_qatar` respectively. Exhibits contains regualr written Markdown files, so it only needs `output: true` in its config. The collection you'be been building in the last few steps is a Wax image/media collection and needs more info to be processed.

You'll need to open the `_config.yml` file and change the following:
* Replace`qatar` with your actual collection name, in all lowercase characters.
* Replace `qatar_item` with whatever you renamed the layout `qatar_item` in the `_layouts` folder to be.
* Replace `qatar.csv` with your metadata file name.
* Replace `raw_images/qatar` with the filename of your folder of item files. 


```
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
```      
| variable      | type accepted	| description	                                                    | used by      |
|:--------------|:------------- |:----------------------------------------------------------------|:-------------|
|collections    |hash           |the site collections                                             |wax and jekyll|
|output         |true/false     |whether or not to output the collection to HTML.                 |jekyll        |
|layout         |string         |which layout in `_layouts` the collection pages should use.      |wax and jekyll|
|metadata:source|string         |path to the collection’s metadata file within the _data directory|wax           |
|images:source  |string         |path to the collection’s directory of images within `_data`      |wax           |

## Search settings
The search variable can create multiple indexes, though just one (main) is recommended. For Wax to use search it needs to a search index, which will be saved as a JSON file. You must change the name of the collection below from `qatar` to your collection name.

```
search:
  main:
    index: '/search/index.json' # file the index will get written to
    collections:
      qatar:
        content: false # whether or not to index page content
        fields: # the metadata fields to index
          - artist
          - location
          - label
          - _date
          - object_type
          - current_location
```
| variable |	type accepted	| description	| used by |
|:-------- | :-------- | :-------- |      :-------- |
| index	| string | the path (within the root of the site) to write the index to | wax |
| collections	| hash |	which collections (as defined in collections above) will be indexed	| wax |
| content	| true/false |	within a collection: whether or not to index the page content in addition to the metadata in the front matter	| wax |
| fields	| list |	within a collection: the metadata fields to index |	wax |

## Menu settings
The menu defined in `_config.yml` is used in the site’s header. This is the navigation bar that will appear at the top of the screen on all pages.

```
menu:
  - label: 'About'
    sub:
      - label: 'Wax'
        link: '/about/'
      - label: 'Documentation'
        link: 'https://minicomp.github.io/wiki/#/wax/'
      - label: 'Credits'
        link: '/credits/'
  - label: 'Exhibits'
    sub:
      - label: 'Local and Remote IIIF Manifests'
        link: '/exhibits/a/'
      - label: 'Inline Parallax Image'
        link: '/exhibits/b/'
      - label: 'Inline Image References'
        link: '/exhibits/c/'
  - label: 'Browse'
    link: '/collection/'
  - label: 'Search'
    link: '/search/'
  - label: 'Reuse'
    link: '/reuse/'
```
| variable |	type accepted	| description	| used by |
|:-------|:-----|:-----|:-----|
| menu | list	| list of menu items | wax |
| label |	string	| the human-readable label for the link or dropdown	| wax |
| link |	string	| the relative (internal) or absolute (external) link |	wax |
| sub	list|	a list of sub items for a dropdown	| wax |

## Footer settings
The theme’s footer uses the site’s title, description, and copyright by default and optionally takes a list of navigation links and logos from the variables below.

footer:
  links:
    - label: 'GitHub'
      link: 'https://github.com/minicomp/wax'
    - label: 'Credits'
      link: '/credits'
    - label: 'Contact'
      link: 'https://gitter.im/minicomp/wax/'
  logos:
    - img: '/assets/logo.png'
    - img: 'https://example.com/logo.png'
      link: 'https://example.com'
