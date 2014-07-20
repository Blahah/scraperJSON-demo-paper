The need to mine content from the scholarly literature at scale is inhibited by technical and political barriers. Publishers have partially addressed this by providing application programming interfaces (APIs). However, we observe that many publisher APIs come with unrealistic restrictions, and that while only a few publishers provide APIs, almost all publishers make their content available on the web. With current web technologies it should be possible to harvest and mine the entire scholarly literature as it is published, regardless of the source of publication, and without using specialised programmatic interfaces controlled by each publisher. To address this challenge as part of the ContentMine project we developed the following tools:

* scraperJSON, a standard for defining reusable web scrapers as JSON objects
* thresher, a web scraping library that uses scraperJSON scrapers and headless browsing to handle many idiosyncrasies of the modern web
* quickscrape, a command-line web scraping suite that uses Thresher
* a library of scraperJSON scrapers to extract data and metadata from many academic publishers

We will demonstrate the use of this stack for scraping the scholarly literature.