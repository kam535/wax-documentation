---
layout: default
title: "Creating your metadata file"
parent: Building your collection
nav_order: 3
---
**Table of Contents**
1. TOC
{:toc}

## What is metadata?
Metadata is literally “data about data”. μετα is a Greek preposition and prefix meaning “with”, “next to”, “after”, or “beside”, so meta + data is data with data. You see metadata all the time and probably don’t realise it. One example of metadata are the labels that you see next to artworks in museums.
<a data-flickr-embed="true" href="https://www.flickr.com/photos/ebarney/5312897134/in/photostream/" title="Museum Label: My Daughter Gladys"><img src="https://live.staticflickr.com/5005/5312897134_c01d45e3d5_k.jpg" width="2048" height="1536" alt="Museum Label: My Daughter Gladys"/></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>
These labels describe a piece of art briefly by listing the artist, the title of a work, the place of origin, the date, and other descriptive information that gives you context about the work. This information is often called tombstone information. Museum labels sometimes have longer descriptions of the work too. You can think about creating metadata for your collection items like creating tombstone information and descriptions for them.

The difference between print metadata and metadata for a digital collection, however, is that a computer doesn’t innately understand that “Irving R. Wiles”, for example, is the name of the artist who created the work or that “oil on canvas” is the medium. This is where metadata schema come in. Each metadata scheme consists of a list of fields, which are the categories that pieces of metadata about a work fall into. For example, “artist” would be a field and “Irving R. Wiles” would be the value that is filled in for that field.

Metadata schema also usually contain rules for how the values in each field are structured and arranged, like whether they’re uppercase or lowercase, can include punctuation, should be abbreviated, and more. Metadata fields also have to be specific enough to at least distinguish all of the items in a collection from one another. For example, only having the fields “colour” and “medium” for a collection of red ceramic vases is pointless, since the metadata would look exactly the same for every single item.

To create a collection, you’re going to have to come up with your own metadata scheme by coming up with a list of fields that you want to use to describe your items. The Wax documentation lists which metadata fields are required, recommended, and discouraged/forbidden (the latter may conflict with files that Wax’s processes in the command line will overwrite). Once you’ve done that, proceed to the next section.

## **Creating your metadata file**

If you’re an advanced computer user, you can skip this section, as you’ll likely be able to make your own file from scratch.

Now that you’re familiar with metadata and have your list of fields, it’s time to create your metadata file and assign some values. Most collections metadata is arranged in tables or spreadsheets, where the top row contains the list of fields and the rows after contain the metadata for each individual object. You can see an example of this in the [Wax documentation’s Metadata file section](https://minicomp.github.io/wiki/wax/preparing-your-collection-data/metadata/). For the sake of simplicity, this guide will show you how to create a tabular metadata file.

You can choose any spreadsheet tool you want to create your metadata. Some spreadsheet tools that are good for beginners and easy to access are: Numbers (on Mac) and Google Sheets. Excel is not recommended by the Wax devs due to bugs.

Some guidelines for what you can put in values:

* You must include a value for each item in [Wax’s required fields](https://minicomp.github.io/wiki/wax/preparing-your-collection-data/metadata/).  
* All values *except for the pid* do not need to be unique  
* Values in the pid field **must** be unique

When you have your file open:

1. List out your metadata **fields** across the top row of the spreadsheet. I recommend putting the pid field in the first column, first row (box A1).  
2. In the column that has the pid field, list out the identifiers for each item in each row down the column (A2, A3, A4, etc.). **You’ll be creating a new row for each item.** Don’t include file extensions in the pid value (.jpg, .pdf, etc.).  
3. Fill out the rest of the values for each item, according to the field that’s in each column.  

| pid          | title                         | location       |
|:-------------|:------------------------------|:---------------|
| obj1         | Parchment fragment on f. 200v | Ithaca, NY     |
| obj2         | AM [aman. frag.               | Ithaca, NY     |
| obj3         | Bonaventure's Lyffe           | Ferrara, Italy |
| obj4         | Fragment in Greek             | unknown        |

Once you have your completed metadata file, I recommend using [OpenRefine](https://openrefine.org) or another data cleanup tool to make sure your spreadsheet is ready to be read by a computer. Once it’s clean, you can download your metadata file. **Make sure the name of your metadata file is the same as the title of your collection.** For example, if my collection title is redvases, I’d name my metadata file redvases.csv. The recommended file type is a CSV (Comma Separated Values), but Wax also accepts YML, JSON, MD, and other file types. If you created a spreadsheet, you’ll have to download your metadata as a CSV.
