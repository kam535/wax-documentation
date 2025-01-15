---
title: Adding your collection data
layout: default
parent: Setting up your site
nav_order: 2
---
## **Adding your collection data**

Now that you’ve cleaned up your project repository, you can add your collection data. You can distinguishes where the parts of your collection data go using the following table:
| folder            | purpose                                   |
|:------------------|:------------------------------------------|
| `_data`           | where raw, unprocessed metadata files go. |
|`_data/raw_images` | where raw, unprocessed image files go.    |


Add your collection items by dragging your folder of item files into the `_data/raw_images` folder of your project repository.

Add your collection metadata by dragging your metadata file into the `_data` folder. Note that it’s best practice to create a copy of this metadata file in the `_data` folder named “original” or something similar. You should **never** edit this original metadata file, as it will serve as a backup in case something goes wrong when you’re editing your main metadata file.

After you’ve added your collection data, you’ll want to go into your files and configure your site to recognize these new folders. See the [Updating your configuration section of the Wax documentation](https://minicomp.github.io/wiki/wax/setting-up-your-site/updating-your-configuration/).
