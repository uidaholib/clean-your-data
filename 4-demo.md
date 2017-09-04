---
layout: default
title: 4-Demo
nav: true
---

# Demo: University Data

In this demo we are going to play with a data set about University endowments harvested from Wikipedia—so it is very *messy*! 

Download <a href="images/universityData.csv" target="_blank">`universityData.csv`</a>

> The university endowment demo data is from the [Enipedia OpenRefine Tutorial](http://enipedia.tudelft.nl/wiki/OpenRefine_Tutorial). 

- Create project 
    - check character encoding, options
    - Refine never over writes your original data, it creates a copy!
    - information is *not* sent over internet

- Column basics
    - text filter
    - faceting
    - edit cells / facets
    - transform, `value.unescape('url')`, find & replace, `value.replace("old","new")`
    - undo/redo
    - clustering
	- split into multiple columns
    - combine columns (*tricky* because combining blank cells results in an error)
        - facet by blank, combine only non-empty cells
        - transform, `value + " " + cells["col 2"].value`
    - remove / reorder columns 

- Export basics
	- OpenRefine project
    - many formats!
    - templating
	- export is always a new copy of data, never alters original!
	
- Automate basics
	- Undo/Redo copy `Extract` to txt file (use text editor, not Word)
	- create new project with original file
	- Undo/Redo paste saved extract into `Apply` 

- More!
	- Star / Flag & remove rows
	- create new column with transform `length(value)`, numeric facet
	- deduplicate
		- sort by, permanent reorder
		- blank down / fill down 
    - fetch URLs
        - basic geo code lookup, `"http://maps.google.com/maps/api/geocode/json?sensor=false&address=" + escape(value, "url")
with(value.parseJson().results[0].geometry.location, pair, pair.lat +", " + pair.lng)`

# Demo: Web Scrape Craigslist 

- Create new project from Clip board
    - paste in `https://pullman.craigslist.org/search/sss`
- create column by fetching url, named "search"
- on "search" column: 
    - create column based on called "links", using transform to get only the \<a\> with class="hdrlnk", `forEach(value.parseHtml().select("a.hdrlnk"),e,e.htmlAttr("href")).join(" ; ")`
- remove the first column and "search" column
- on "links" column: 
    - split multivalued cells on `;`
    - add links with transform, `"https://pullman.craigslist.org"+value`
    - add column by fetching url, named "ads"
- on "ads" column:
    - get title: add column based on "ads" named "title", grabbing span class="postingtitletext", `value.parseHtml().select("head")[0].select("title")[0].htmlText()`
    - get price: `value.parseHtml().select("h2.postingtitle")[0].select("span.price")[0].htmlText()`
    - get category: `value.parseHtml().select("header")[0].select("li.category")[0].htmlText()`
	
Etc!


