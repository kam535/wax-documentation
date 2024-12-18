---
title: FAQ & Troubleshooting
layout: default
nav_order: 9
---
* Q: I just set up my site and none of my images are loading in the gallery. What should I do?  
* A: The first step would be to go into your \_config.yml file and make sure your collection settings are correct.   
  * Make sure the title of your collection matches the name of your metadata file.  
  * Make sure you changed the name of the qatar\_item.html layout to reflect your collection title. Make sure you update the qatar\_item.html file and the \_config.yml file with this change.  
  * Make sure you’ve included the name of your metadata file in the metadata \> source field.  
  * Make sure you’ve included the path to your images folder in the images \> source field.   
  * Make sure all of your single quotes ‘ ‘ are in the right place.  
* Suggestion two would be to check your img folder to make sure your image derivatives are uploaded correctly.   
* Suggestion three would be to check to make sure your image filenames match your item pids exactly (sans the file extension). If none of these work, contact the Wax devs for support.
