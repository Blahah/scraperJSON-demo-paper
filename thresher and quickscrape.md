## thresher

Thresher is a Node.js web scraping library that uses scraperJSON scrapers. By harnessing the url specification in scraperJSON, thresher can scrape long lists of URLs and automatically choose the best scraper for the task from a provided collection of scrapers. Thresher supports the optional user interaction feature in scraperJSON by rendering webpages and performing actions in PhantomJS, a headless WebKit browser, if interactions are specified.

To encourage responsible scraping, and to avoid triggering denial of service by publishers, thresher implements a domain-based rate limit. A separate queue of URLs to be scraped is maintained for each domain, and the queues are processed in parallel.

Because much of the scholarly literature is behind a pay-wall, thresher allows sets of cookies to be used to authenticate with websites during scraping.

## quickscrape

Quickscrape (http://github.com/ContentMine/quickscrape) is a cross-platform command-line suite that provides access to all the functionality of thresher.