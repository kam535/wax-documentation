---
layout: default
title: File breakdown
nav_order: 7
---
## **File breakdown**
{:toc}

It’s important to understand what files do what in your repository so you’ll know what to edit where and can troubleshoot issues more easily. Files that are essential to the functioning of the site are highlighted. Here’s a breakdown of what each file in each folder does:

### **`.github`**

This folder, and all of the files it contains, are used when you serve the site using GitHub Actions instead of directly through the main branch of your site. If you’ve already served your site through GitHub Pages and intend to keep it that way, you don’t need this file. If you want to know more, please see the [GitHub Actions section of the Jekyll documentation](https://jekyllrb.com/docs/continuous-integration/github-actions/).

### **`\_data`**

This folder contains all of the core information, including the metadata file and image directory, for your site. I don’t recommend you change anything in here from the GitHub.com interface, since If you change anything in here, you’ll need to individually change things in a bunch of other files.

* `**raw\_images**`: This folder contains the raw image files for your collection items.  
* `**yourcollectiontitle.csv`:** Your collection’s metadata file(s).  
* `**original.csv`:** Your collection’s original, unaltered metadata file(s).

### **`_exhibits`**

This folder contains the files that will make up your exhibit pages. Exhibits are just pages that can highlight certain aspects of your collection with a combination of images and text, just like an in-person gallery. For an example, see the [Wax demo site](https://minicomp.github.io/wax/exhibits/a/). These files are usually written in Markdown with Jekyll front matter.

### **`_includes`**

This folder contains all of the includes for the site. An include is a file that can have its contents pulled using a specific line of code (an include statement) into another file. Include files typically contain the code for an element, tool, or feature of a site, like a gallery, a word cloud, or a timeline. To call an include, you’ll add the an [include tag](https://jekyllrb.com/docs/includes/) to the code of your page. For more on includes, see the [Includes section of the Jekyll documentation](https://jekyllrb.com/docs/includes/).

* **`collection_gallery.html`**: Creates a clickable, filterable gallery of thumbnail images of your collection. See the [Browse page on the Wax demo site](https://minicomp.github.io/wax/collection/).  
* **`footer.html`:** The code for the footer (bottom section) of each page of the site.  
* **`head.html`:** Contains the metadata for the site.  
* **`header.html`:** The code for the header (top section with title and navbar) of each page of the site.  
* **`inlineimage.html`**: Serves and formats a specified image in the middle of text on a page.  
* **`interactive_metadata_table.html`**: Creates an interactive data table from a collection metadata file. See the [Reuse page on the Wax demo site](https://minicomp.github.io/wax/reuse/).  
* **`item_metadata.html`**:   
* **`item_pagination.html`:**  
* **`osd_iiif_image_viewer.html`**: Generates a mini IIIF viewer to view an IIIF image derivative from the img/derivatives folder.  
* **`parallax_image.html`**: Serves and formats an image in a shifting parallax bar across the screen.   
* **`search_box.html`**: Generates a search box on the page to search content.  
* **`simple_image_viewer.html`**: Generates a viewer to view a simple image derivative (png and jpg) from the img/derivatives folder.

### **`_layouts`**

This folder contains preset layouts for the content on different pages. You can include a layout in the front matter of a page and any content on that page will be displayed according to the layout.

* **`default.html`**: The default layout for any page. It’s the base for all other layouts.  
* **`exhibit.html`**: A layout for exhibit pages. It displays page metadata like a blog post, including the exhibit author’s name, the exhibit date, and the exhibit title.  
* **`generic_collection_item.html`**: The general layout for each individual collection item page in your collection page folder (`_yourcollectionname`). It’s the base template for the `qatar_item.html` layout in the Wax demo repository (or `yourcollectionname_item.html`).  
* **`page.html`**: The layout for all other non-exhibit pages on the site.

### **`_sass`**

The `_sass` folder contains the stylesheets (Syntactically Awesome Style Sheets and Cascading Style Sheets) that determine all of the stylistic/aesthetic elements of the site. I highly suggest not messing with these folders until you become more familiar with Wax, Jekyll, web-building, and JS, HTML, and CSS.

* **`_boostrap.css`:** Contains all of the Bootstrap styles. Bootstrap is a huge CSS framework and library.  
* **`_wax.css`:** Contains all of the styles that are custom for Wax.

### **`assets`**

The `assets` folder contains all of the Javascript scripts and some CSS files that style the elements produced and run by those scripts. As with the `_sass` folders, I highly suggest not messing with these folders until you become more familiar with Wax, web-building, and JS, HTML, and CSS.  
bootstrap

* **`datatables`:** This folder contains the Javascript file and CSS file that run and display the `interactive_metadata_table.html` include.  
* **`openseadragon:`** This folder contains all of the button, images, icons and Javascript files that run and display the `osd_iiif_image_viewer.html` include.  
* **`default.png`:** The default thumbnail image for a collection item, when the image included in the `raw_images` folder for an item is missing or broken.  
* **`elasticlunr.min.js`:** The Javascript file that runs elasticlunr, a lightweight full-text search engine that’s behind the search bar queries on the site.  
* **`jquery-3.2.1.min.js`:** A Javascript file that enables the use of jQuery, a Javascript library that enables the use of contained methods that reduce the amount of code you have to use to do something.  
* **`popper.min.js`:** A Javascript file that runs Popper, a positioning engine for tooltips/HTML elements.  
* **`search-ui.js`:** A Javascript file that runs the user interface for search bars on the site.  
* **`styles.scss`:** More CSS for particular elements.

### **`img`** 

The img folder contains all the derivative images for the collection items, as generated by the Wax derivatives task.

### **`pages`**

The pages folder contains most of the page files for the site, with the exception of the homepage. You can create a new page by creating a new Markdown (.md) file in this folder. Pages all have Jekyll front matter specifying their permalink or URL.

You can change the contents of any page on the site and add new pages by writing new content using Markdown, adding new includes, and setting up your page using the front matter. For this reason, this guide will not list the contents of the default template pages.

### **`search`**

The search folder contains the search index file that determines how the elasticlunr search finds content on the side. The `index.json` file is produced by the Wax search task.

### **`index.md`**

The `index.md` file is the front or home page of the site. It does not have a permalink in the demo and is the default page associated with your repository’s GitHub Pages. You can edit it like any ordinary page. See the [home page of the Wax demo site](https://minicomp.github.io/wax/).

### **`.gitignore`, `.ruby-version`, `Dockerfile`, `Gemfile`, `Rakefile`, `wax\_theme.gemspec`**

All of these files can be summed under the bucket of “back-end setup”. These files support the Ruby Gem, Wax theme, and setup and files for GitHub Pages to ignore when serving the site.

### **`LICENSE.txt`**

This text files includes the license under which Wax can be shared and used.

### **`README.md`**

This file just contains the instructions for using Wax. You can delete this if you want.

### **`_config.yml`**

The `_config.yml` file controls the configuration and settings for various elements on the site, including navigation/menu, the title and description, URL and base URL, copyright information, site logo, the default thumbnail image for items in a gallery, the organization of collections and exhibits, build settings, search settings, and footer links and logos. 
