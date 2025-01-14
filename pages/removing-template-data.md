---
layout: default
title: Removing template data
parent: Setting up your site
nav_order: 1
---
### **Removing template data**

Once you have your new template repository, you’ll need to make some changes to remove the template data and add your own. The first step is to remove all of the basic template data and derivatives:

1. Open the command line (Terminal, Linux CMD, or Windows CMD/PowerShell)  
2. In the command line, navigate to the directory where you have your cloned project folder.  
3. Paste the following into the command line: `bundle exec rake wax:clobber qatar`  
4. Alternatively, you can open your project folder in the Finder or File Explorer GUI and delete the following directories and files:  
   * `_qatar`  
   * anything in `img/derivative`s  
   * `_data/qatar-original.csv  `
   * `_data/qatar.csv`  
   * anything in `_data/raw_images` 
   * `search/index.json`

You’ll also need to edit the following files to replace any instances of “qatar” with your new collection title. Your collection title should be the same as the name of your metadata file:

* `_config.yml`  
* `index.md`  
* `collection.md`  
* `reuse.md`  
* `qatar_item.html`  
  * You’ll need to rename this to match your collection and change any instances of “qatar” in the file to your new collection name.

After you’ve edited these files, you’re probably still going to need to search your code for the word “qatar”, since there may be other instances where the template collection is lurking. You can do this by searching for “qatar” in your project folder using the Finder or File Explorer GUI or by searching for “qatar” in your repository on GitHub.
