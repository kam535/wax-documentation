---
title: Data downloads
layout: page
nav_order: 4
parent: WaxBuilder
---
# Data downloads
The data downloads is a heavily Frankensteined and simplified version of the Collection Data section of CollectionBuilder. This allows users to download the data from your site as a CSV (metadata), JSON (metadata), Facets JSON (when there are facets), GeoJson (from the map), JSON (timeline), or the whole repo with all of the code. This page is managed with the following files:
* `_data/data-settings.yml`
* `_includes/interactive_metadata_table.html`
* `assets/data-tables.css`
* `assets/data-tables.min.js`
* `geodata.json`
* `facets.json`
* `timelinejs.json`

## data-settings.yml
This file lets you specify which fields you want to export from your metadata spreadsheet for the CSV, JSON, and Facets JSON downloads.

## interactive_metadata_table.html
The main include that generates the dropdown and interactive table of metadata from your metadata spreadsheet on the Data page. Relies on `data-tables.min.js`.

## data-tables.css
The styling for the data table.

## geodata.json
The template that the GeoJson data for the map page populates into.

## facets.json
The template that the JSON data for the facets you specify in `data-settings.yml` populates into.

## timelinejs.json
Currently under development. The template that the JSON data for the timeline populates into.

## Creating a data download page
To create a data page, simply create a new markdown file in the `_pages` repository. Set the layout to `page` and the `collection` to your collection name in the Jekyll front matter. Add the `interactive_metadata_table` include to the content of your markdown file and add `collection=page.collection` as a parameter to your include.
