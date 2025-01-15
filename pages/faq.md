---
title: FAQ & Troubleshooting
layout: default
nav_order: 9
---
Q: I just set up my site and none of my images are loading in the gallery. What should I do?  
A: The first step would be to go into your `_config.yml` file and make sure your collection settings are correct.   
  * Make sure the title of your collection matches the name of your metadata file.  
  * Make sure you changed the name of the `qatar_item.html` layout to reflect your collection title. Make sure you update the `qatar_item.html` file and the `_config.yml file` with this change.  
  * Make sure you’ve included the name of your metadata file in the metadata > source field of the `_config.yml file`.  
  * Make sure you’ve included the path to your images folder in the images > source field of the `_config.yml file`.   
  * Make sure all of your single quotes ‘ ‘ are in the right place.  
  * Check your `img` folder to make sure your image derivatives are uploaded correctly.   
  * Check to make sure your image filenames match your item pids exactly (sans the file extension). If none of these work, contact the Wax devs for support.

General troubleshooting tips:
* When something goes wrong, check the `_config.yml` file and your collections sites first. Make sure your sources are correct for metadata and images. Make sure there aren't any typos.
* If something looks off with your individual collection item pages, check the Jekyll front matter for that page. Make sure there aren't any typos and that your metadata on the page matches the metadata in your metadata file.
* Make sure you're running the Wax tasks every time you make changes to a file, add an image, or add a collection item. You'll need to update the search index, pages, and derivatives each time you make a change that would affect the metadata of the collection.

### Get help
You can get help for all of your Wax-related problems and questions by joining the [Code4Lib Slack](https://docs.google.com/forms/d/e/1FAIpQLSeD77mBp0Y13mFePF8UmDwFrlbxNx3VttEjz_3dgglJeK-Zbg/viewform?c=0&w=1) and the **#minicomp-wax** channel. You can also reach out to the editor of this documentation, Kiran, at kam535@cornell.edu for help.
