## scraperJSON
We defined a new JSON schema, scraperJSON, to enable declarative scraping of structured data from many different sites without duplicating code. A scraperJSON scraper consists of a JSON object with a minimum of two keys:

* ***url***: an array of regular expressions specifying the sites to which the scraper can apply
* ***elements***: an object specifying the elements to be extracted

*Elements* are objects specifying either a selector or one or more child elements, and optionally an attribute and some configuration. *Selectors* may be CSS, XPath, or follow the Open Annotation standard. This simple system allows for the capture of the majority of metadata from scholarly articles.

### Simulating user interaction

Many modern websites do not specify their content in the raw HTML served when a URL is visited, but lazy-load the content, for example by making AJAX calls. These loading events are triggered by user interactions such as scrolling and clicking. To enable to scraping of full content, we therefore added the ability to specify user interactions to scraperJSON. 

### Structuring results

The structure of the scraperJSON *elements* object defines the structure of the results. Thus, each key in the *elements* of the scraper will be reflected as a key in the *elements* of the results. Elements can contain other elements, so that the results of the child elements are grouped into objects reflecting the structure of the parent element. This allows powerful capture of structured data representing entities and their properties, such as the name, affiliation and email of an author.

### Downloads

When scraping the scholarly literature, it is usually of interest to download files such as fulltext PDFs and HTML, XML and RDF documents where available, and to capture full-sized figure images and supplementary materials. This feature is supported in scraperJSON. Elements specifying URLs can have their target(s) downloaded and optionally renamed to a specified format.

### Nested scrapers

Content associated with a page is often available in a more extensive form in a linked resource. This is observed with full figures on the websites of many acadmic publishers, where a thumbnail is displayed in the article and a link must be followed to expose the full image. This situation can be handled in scraperJSON: if an element targets a URL, the URL can be followed and one or more child elements extracted.

A scraperJSON scraper demonstrating all the described features is shown in figure 1, along with the results of an example scraping operation. The scraperJSON specification is available on Github: https://github.com/ContentMine/scraperJSON.