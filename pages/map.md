---
title: Interactive map
layout: page
nav_order: 1
parent: WaxBuilder
---
# Interactive map

The interactive map is a feature of WaxBuilder taken and modified from the CollectionBuilder source code (thank you, Devin Becker). The map is a basic Leaflet map with cluster features. All map features are managed by the following files:
* _includes/map-js.html
* _layouts/map.html
* _data/map-settings.yml
* _data/config-map.csv

## map-js.html
This is the file that create geojson data from your CSV file and creates and runs the map itself.

## map.html
This layout calls the **map-js.html** include on a standard page template. This is the layout you'll use in the front matter of your map page.

## config-map.csv
This file lets you pick which fields you want to appear in the popup for each marker on the map. By default, your popup will include the thumbnail image for an object that links out to each object page when clicked on. In column one of the config table, specify the fields from your metadata spreadsheet that you want to see in the popup. In column two, specify how you want that field to appear in the popup (this doesn't have to be the same as your metadata spreadsheet). In the third column, specify whether you want these fields to appear when you enter a query in the map search bar or not (true or false).

## map-settings.yml
This file is where you'll specify layout and styles for the map, though you can also do this simply by editing the `map-js.html` file. This includes the default zoom for the map, whether clusters appear, the base map, etc.

## Creating a map page
To create a map page, simply create a new markdown file in your pages directory. Set the layout in the Jekyll front matter to map. You can add any content you'd like above or below the map as you choose. By default, WaxBuilder has nothing above or below the map.

I am currently working on consolidating these files in the future.

