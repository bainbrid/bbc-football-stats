# BBC Football Stats Scraper

This project uses the scrapy web scraping framework (http://scrapy.org) to scrape data from the BBC Sport website (http://www.bbc.com/sport/0/football/).
You can use this to collect data about any football club available on the BBC site, including recent results, fixtures, and table position.

## Installation

After cloning this repository, you'll need to install scrapy. The downloads and subsequent instructions are available here: http://scrapy.org/download/.

## Usage

Once everything is installed and ready to go, you can check out the available spiders in `footballstats/spiders/stats_spider.py`

**IMPORTANT:** You must pass **TEAM\_NAME** and **LEAGUE\_NAME** as environment variables (see `footballstats/spiders/stats_spider.py` for more instructions) for the team you want data on and its league.

I recommend reading through the scrapy documentation (http://doc.scrapy.org/en/0.24/intro/tutorial.html) about how to use scrapy scrapers, but below is an example use case.

First navigate to the root folder, then use the following command:
> scrapy crawl results -o results.json

This will output the past results available from the club's BBC page into a JSON file called results.json, looking like:
> {"date": " Sun 28 Dec ", "awayTeam": "Bolton", "homeTeam": "Huddersfield", "score": " 2-1 ", "competition": " Championship  "} 

Just replace 'results' in that command with the name of other spiders in order to invoke them.

## Contact

If you run into bugs, or have any comments or questions, feel free to create an issue within the GitHub Issues page. 
