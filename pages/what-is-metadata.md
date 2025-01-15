---
title: What is metadata?
layout: default
parent: Building your collection
nav_order: 2
---

Metadata is literally “data about data”. μετα is a Greek preposition and prefix meaning “with”, “next to”, “after”, or “beside”, so meta \+ data is data with data. You see metadata all the time and probably don’t realise it. One example of metadata are the labels that you see next to artworks in museums.   
[![][image1]](https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.flickr.com%2Fphotos%2Febarney%2F5312897134&psig=AOvVaw1-YW5rpwLMSptJW3NPbZyC&ust=1734190772749000&source=images&cd=vfe&opi=89978449&ved=0CBQQjRxqFwoTCPjbrZmKpYoDFQAAAAAdAAAAABAE)  
These labels describe a piece of art briefly by listing the artist, the title of a work, the place of origin, the date, and other descriptive information that gives you context about the work. This information is often called [tombstone information](https://projects.iq.harvard.edu/classicswrites/tombstone-information). Museum labels sometimes have longer descriptions of the work too. You can think about creating metadata for your collection items like creating tombstone information and descriptions for them.

The difference between print metadata and metadata for a digital collection, however, is that a computer doesn’t innately understand that “Irving R. Wiles”, for example, is the name of the artist who created the work or that “oil on canvas” is the medium. This is where **metadata schema** come in. Each metadata scheme consists of a list of **fields**, which are the categories that pieces of metadata about a work fall into. For example, “artist” would be a field and “Irving R. Wiles” would be the **value** that is filled in for that field. 

Metadata schema also usually contain rules for how the values in each field are structured and arranged, like whether they’re uppercase or lowercase, can include punctuation, should be abbreviated, and more. Metadata fields also have to be specific enough to *at least* distinguish all of the items in a collection from one another. For example, only having the fields “colour” and “medium” for a collection of red ceramic vases is pointless, since the metadata would look exactly the same for every single item.

To create a collection, you’re going to have to come up with your own metadata scheme by coming up with a list of **fields** that you want to use to describe your items. The Wax documentation lists which [metadata fields are required, recommended, and discouraged/forbidden](https://minicomp.github.io/wiki/wax/preparing-your-collection-data/metadata/) (the latter may conflict with files that Wax’s processes in the command line will overwrite). Once you’ve done that, proceed to the next section.
