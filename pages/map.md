---
title: Interactive map
layout: page
nav_order: 1
parent: WaxBuilder
---
The interactive map is a feature of WaxBuilder taken and modified from the CollectionBuilder source code (thank you, Devin Becker). All map features are managed by the following files:
* _includes/map-js.html
* _layouts/map.html
* _data/map-settings.yml
* _data/config-map.csv

## map-js.html
This is the Javascript that runs the map itself.

## map.html
This layout calls the **map-js.html** include on a standard page template. This is the layout you'll use in the front matter of your map page.


I am currently working on consolidating these files in the future. 
