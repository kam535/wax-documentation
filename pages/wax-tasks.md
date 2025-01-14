---
title: Running Wax tasks
layout: default
parent: Setting up your site
nav_order: 3
---

## **Generating and adding derivatives, search info, and object pages**

Wax has three tasks that automatically generate thumbnail and full image derivatives, individual pages, and search information for for your collection items. You'll need to run these tasks in your command line. **Note that much of the following content is copied from the Wax documentation and should be credited to Minicomp.** If you are building your project using Docker, you **must** see the [Running the main tasks section of the Wax Documentation](https://minicomp.github.io/wiki/wax/running-the-tasks/#running-the-main-tasks). Note that before running any tasks, you'll have to update your site's configuration in the _config.yml file first.

### Table of Contents
1. TOC
{:toc}

### wax:derivatives
There are two types of derivatives for Wax: simple and iiif. Simple derivatives will be produced in `.jpg` format. IIIF derivatives are produced as individual IIIF-compliant image tiles, canvases, collections, and manifests. If you're unfamiliar with IIIF, see the [IIIF website](https://iiif.io) for more information. If your collections include AV, multimedia, 3D, or pdf objects, you **must** use IIIF derivatives.

#### wax:derivatives:simple
To run the task, simply run the following command in the command line: `bundle exec rake wax:derivatives:simple YOUR_COLLECTION_NAME`
<br>
<br>
YOUR_COLLECTION_NAME should be replaced with the name of the collection you're running the task for. This task will produce image derivatives in the `img/derivatives/simple` folder of your project repository, including both a `full` and `thumbnail` image. It will also add the short URLs to these images to your items' metadata records.

#### wax:derivatives:iiif
To run the task, simply run the following command in the command line: `bundle exec rake wax:derivatives:iiif YOUR_COLLECTION_NAME`
<br>
<br>
YOUR_COLLECTION_NAME should be replaced with the name of the collection you're running the task for. This task will produce image tiles, json manifest files, and IIIF derivatives in the `img/derivatives/iiif` folder of your project repository, including both a `full` and `thumbnail` image. It will also add the short URLs to these images to your items' metadata records.

### wax:pages
The Wax pages task generates an individual page for each item in your collection, in a folder titled `_YOUR_COLLECTION_NAME`. These pages display individually on your project site as the main page for each object.
<br>
<br>
To run the task, run the following command in the command line: `bundle exec rake wax:pages YOUR_COLLECTION_NAME`.
<br>
YOUR_COLLECTION_NAME should be replaced with the name of the collection you're running the task for. This task will produce Markdown files for each item in your collection, named after each item's `pid`.

### wax:search
The Wax search task generates an index for thr search feature of your site so that you can search for items by any of the metadata fields included in your metadata file.
<br>
<br>
To run the task, run the following command in the command line: `bundle exec rake wax:search SEARCH_NAME`. Unless you've changed it in your `_config.yml` file, SEARCH-NAME should be replaced with **main**.
