## **Scraping software: _thresher_ and _quickscrape_**

***thresher*** (http://github.com/ContentMine/) is a web scraping library that uses scraperJSON scrapers. It is written in Node.js and released under the MIT license.

### Automatic scraper selection

By harnessing the url specification in scraperJSON, thresher can process lists of URLs and automatically choose the best scraper for each from a provided collection of scrapers. 

### Headless rendering

Headless browsers are Thresher supports the optional user interaction feature in scraperJSON by rendering webpages and performing actions in PhantomJS, a headless WebKit browser, if interactions are specified.

### Rate-limiting

To encourage responsible scraping, and to avoid triggering denial of service by publishers, thresher implements a domain-based rate limit. A separate queue of URLs to be scraped is maintained for each domain, and the queues are processed in parallel.

### Authentication

Because much of the scholarly literature is behind a pay-wall, thresher allows authentication by one of three commonly used methods:

1. using HTTP login/password authentication
2. using a proxy
3. by providing a set of session cookies

## quickscrape

***quickscrape*** (http://github.com/ContentMine/quickscrape) is a cross-platform command-line suite that provides access to all the functionality of thresher.