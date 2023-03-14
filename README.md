# crawls

Crawls and indexes

Located at `/Users/Shared/GitHub/Orgs/TheBoatyMcBoatFace/crawls`

`spider --domain https://civicactions.com crawl -o > spider_civicactions.com.json`

`spider --subdomains --tld --domain https://civicactions.com crawl --output-links > spider_civicactionscom.json`

`spider --subdomains --tld --domain https://civicactions.com crawl -o > civicactions.com.json`

`spider --domain https://civicactions.com scrape -o > scrape_civicactions.com.json`
-s

## Agencies

### NSF

spider --subdomains --tld --verbose --respect-robots-txt --domain https://beta.nsf.gov crawl --output-links > beta.nsf.gov/crawl.json

spider --respect-robots-txt --domain https://beta.nsf.gov scrape --output-links > beta.nsf.gov/scrape.json

### Department of Education

spider --domain https://data.ed.gov scrape --output-links > gov/ed/data_scrape.json

### Department of Veterans Affairs

spider --verbose --domain https://www.va.gov scrape --output-links > gov/va/data_scrape.json

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

spider --subdomains --tld --domain https://beta.nsf.gov crawl --output-links > beta.nsf.gov/scrape.json

spider --domain https://data.ed.gov scrape -s -o > data.ed.gov/scrape.json

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

## Overview

```
madeindjs <contact@rousseau-alexandre.fr>, j-mendez <jeff@a11ywatch.com>
The fastest web crawler CLI written in Rust.

USAGE:
    spider [OPTIONS] --domain <DOMAIN> [SUBCOMMAND]

OPTIONS:
    -b, --blacklist-url <BLACKLIST_URL>
            Comma seperated string list of pages to not crawl or regex with feature enabled

    -d, --domain <DOMAIN>
            Domain to crawl

    -D, --delay <DELAY>
            Polite crawling delay in milli seconds

    -h, --help
            Print help information

    -r, --respect-robots-txt
            Respect robots.txt file

    -s, --subdomains
            Allow sub-domain crawling

    -t, --tld
            Allow all tlds for domain

    -u, --user-agent <USER_AGENT>
            User-Agent

    -v, --verbose
            Print page visited on standard output

    -V, --version
            Print version information

SUBCOMMANDS:
    crawl     crawl the website extracting links
    help      Print this message or the help of the given subcommand(s)
    scrape    scrape the website extracting html and links
bhensel-ca@Bentleys-MacBook-Pro ~ % cd /Users/Shared/GitHub/Orgs/TheBoatyMcBoatFace/crawls
bhensel-ca@Bentleys-MacBook-Pro crawls % spider crawl -h
spider-crawl
crawl the website extracting links

USAGE:
    spider --domain <DOMAIN> crawl [OPTIONS]

OPTIONS:
    -h, --help            Print help information
    -o, --output-links    stdout all links crawled
    -s, --sync            sequentially one by one crawl pages
```

# Crawlee

https://crawlee.dev/docs/quick-start#installation-with-crawlee-cli
