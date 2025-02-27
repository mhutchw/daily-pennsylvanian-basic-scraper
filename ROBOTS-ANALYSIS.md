# Robots Analysis for the Daily Pennsylvanian

The Daily Pennsylvanian's `robots.txt` file is available at
[https://www.thedp.com/robots.txt](https://www.thedp.com/robots.txt).

## Contents of the `robots.txt` file on [ ... date you accessed the file ... ]

```
User-agent: *
Crawl-delay: 10
Allow: /

User-agent: SemrushBot
Disallow: /
```

## Explanation

User-agent: *

This applies to all web crawlers (like Googlebot, Bingbot, and your scraper).
Crawl-delay: 10

This tells crawlers to wait 10 seconds between requests.
It’s a way to prevent excessive load on the website’s servers.
Your scraper should respect this delay (you may need to add a time.sleep(10) in your script).
Allow: /

This means all pages on the site are allowed to be crawled for general bots (except those specifically blocked later).
Your scraper is allowed to access the website.
User-agent: SemrushBot

This targets the SemrushBot specifically.
Disallow: /

This means SemrushBot is not allowed to crawl any part of the website.
Other bots (like yours) are still allowed because the general rule (Allow: /) applies to them.
