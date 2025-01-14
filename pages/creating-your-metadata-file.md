---
layout: default
title: "Creating your metadata file"
parent: Building your collection
nav_order: 3
---

### **Creating your metadata file**

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

<iframe src="https://docs.google.com/spreadsheets/d/e/2PACX-1vR-t1aYB8aH2xsXXUuMqPLpWJmPcOTA3GkCP5cUtGYrk1OGZWxAh6CDo_mqicyAnJ5jxHhU_BRgGPBJ/pubhtml?widget=true&amp;headers=false"></iframe>

Once you have your completed metadata file, I recommend using [OpenRefine](https://openrefine.org) or another data cleanup tool to make sure your spreadsheet is ready to be read by a computer. Once it’s clean, you can download your metadata file. **Make sure the name of your metadata file is the same as the title of your collection.** For example, if my collection title is redvases, I’d name my metadata file redvases.csv. The recommended file type is a CSV (Comma Separated Values), but Wax also accepts YML, JSON, MD, and other file types. If you created a spreadsheet, you’ll have to download your metadata as a CSV.
