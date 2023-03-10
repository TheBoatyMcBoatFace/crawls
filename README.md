# crawls

Crawls and indexes

Located at `/Users/Shared/GitHub/Orgs/TheBoatyMcBoatFace/crawls`

`spider --domain https://civicactions.com crawl -o > spider_civicactions.com.json`

`spider --subdomains --tld --domain https://civicactions.com crawl --output-links > spider_civicactionscom.json`

`spider --subdomains --tld --domain https://civicactions.com crawl -o > civicactions.com.json`

`spider --domain https://civicactions.com scrape -o > scrape_civicactions.com.json`
-s

## Commands

`spider` + Options + `--domain URL` + Subcommands + `-o > DIRECTORY`

```SUBCOMMANDS:
    crawl     crawl the website extracting links
    help      Print this message or the help of the given subcommand(s)
    scrape    scrape the website extracting html and links
bhensel-ca@Bentleys-MacBook-Pro ~ % cd /Users/Shared/GitHub/Orgs/TheBoatyMcBoatFace/crawls
bhensel-ca@Bentleys-MacBook-Pro crawls % spider crawl -h
spider-crawl
crawl the website extracting links
```

`spider --domain https://civicactions.com scrape -o > scrape_civicactions.com.json`

### Scrape

```
spider-scrape
scrape the website extracting html and links

USAGE:
    spider --domain <DOMAIN> scrape [OPTIONS]

OPTIONS:
    -h, --help            Print help information
    -o, --output-links    stdout all pages links crawled
        --output-html     stdout all pages html crawled
```

**_Get Links_**
spider --domain https://civicactions.com scrape --output-links > civicactions.com/scrape.json

spider --domain https://data.ed.gov scrape -o > data.ed.gov/scrape.json

**_Get HTML_**
spider --domain https://civicactions.com scrape --output-html > civicactions.com/scrape-html.json

### Crawl

bhensel-ca@Bentleys-MacBook-Pro spider % spider help crawl
spider-crawl
crawl the website extracting links

USAGE:
spider --domain <DOMAIN> crawl [OPTIONS]

OPTIONS:
-h, --help Print help information
-o, --output-links stdout all links crawled
-s, --sync sequentially one by one crawl pages
