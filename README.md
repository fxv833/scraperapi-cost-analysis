# Data Scraping Tools: What 1,000 Pages Really Cost, Which Plan You Need, and When a Free Library Beats Every API

ScraperAPI's cheapest paid plan is $49/month for 100,000 API credits, and a standard page costs one credit. That is $0.49 per 1,000 pages at the entry tier, roughly three times what the next plan charges for the same page. The free plan gives you 1,000 credits a month, and a 7-day trial adds 5,000 credits without a card.

Those headline numbers are easy to find. The number that decides your bill is the multiplier: a JavaScript-rendered page costs 10 credits, a premium proxy adds 10, a Google SERP costs 25, and ultra premium plus rendering costs 75. On the wrong tier, 1,000 rendered pages cost $12.25 instead of $1.49.

Below are all eight ScraperAPI plans with their credit allowances and concurrency, the real cost per 1,000 pages at three tiers, a comparison against Scrape.do, Zyte, Bright Data, Firecrawl and Apify, and the workloads where you should not buy any of them.

> **Most developers should start on Startup, not Hobby.** Hobby charges $0.49 per 1,000 standard pages; Startup charges $0.15 for the same page and gives you 10x the credits for $100 more. Hobby only makes sense as a paid test. 👉 [See the current plan list and per-credit rates](https://www.scraperapi.com/pricing?fp_ref=coupons)

## What ScraperAPI does, and what it leaves to you

You send a URL; ScraperAPI rotates proxies, spins up a headless browser when the page needs one, handles CAPTCHAs, retries failed requests, and returns the response. Your parsing logic stays in your codebase. Structured endpoints exist for a handful of common targets such as Google and Amazon, but the core product is a fetch-and-unblock layer, not a data product. That matters for pricing: you pay per request, not per record.

Here is the full plan lineup as published.

| Plan | Credits per month | Concurrent threads | Geotargeting | Price | Start |
| --- | --- | --- | --- | --- | --- |
| Free | 1,000 | 5 | US & EU | $0 | [Free plan](https://www.scraperapi.com/pricing?fp_ref=coupons) |
| Hobby | 100,000 | 20 | US & EU | $49/mo | [Hobby, $49/mo](https://www.scraperapi.com/pricing?fp_ref=coupons) |
| Startup | 1,000,000 | 50 | US & EU | $149/mo | [Startup, $149/mo](https://www.scraperapi.com/pricing?fp_ref=coupons) |
| Business | 3,000,000 | 100 | Country-level | $299/mo | [Business, $299/mo](https://www.scraperapi.com/pricing?fp_ref=coupons) |
| Scaling | 5,000,000 | 200 | Country-level | Volume rate | [Scaling plan](https://www.scraperapi.com/pricing?fp_ref=coupons) |
| Professional | 10,500,000 | 300 | Country-level | Volume rate | [Professional plan](https://www.scraperapi.com/pricing?fp_ref=coupons) |
| Advanced | 21,500,000 | 500 | Country-level | Volume rate | [Advanced plan](https://www.scraperapi.com/pricing?fp_ref=coupons) |
| Enterprise | 22,000,000+ | 500+ | Country-level | Custom | [Enterprise quote](https://www.scraperapi.com/pricing?fp_ref=coupons) |

The per-credit rate falls as the allowance grows. Scaling, Professional and Advanced are quoted per credit on the pricing page rather than at a flat monthly figure, and Enterprise is a contract. Divide price by credits for the three self-serve tiers and you get $0.49, $0.15 and $0.10 per 1,000 credits. That ladder is the single most useful number on the page, and it is not printed anywhere on it.

## The multiplier table that decides your bill

One credit equals one standard page request. Everything harder than a standard page costs more, and the pricing page is explicit about how much.

| Request type | Credits | Cost per 1,000 at Startup ($0.149/1K credits) |
| --- | --- | --- |
| Standard page | 1 | $0.15 |
| E-commerce (Amazon, Walmart, eBay) | 5 | $0.75 |
| JavaScript rendering (`render=true`) | 10 | $1.49 |
| Premium proxy (`premium=true`) | 10 | $1.49 |
| Bot-protection bypass (Cloudflare, DataDome, PerimeterX, Akamai) | +10 | $1.49 extra |
| Premium proxy + JS rendering | 25 | $3.73 |
| SERP (Google, Bing, subdomains) | 25 | $3.73 |
| LinkedIn | 30 | $4.47 |
| Ultra premium (`ultra_premium=true`, paid plans only) | 30 | $4.47 |
| Ultra premium + JS rendering | 75 | $11.18 |

Geotargeting, sessions, device type, output format and auto-parsing add nothing. The expensive knobs are rendering, proxy tier and target site.

Now put those credits against the three self-serve price points:

| Workload | Hobby ($0.49/1K credits) | Startup ($0.149/1K) | Business ($0.0997/1K) |
| --- | --- | --- | --- |
| Standard page | $0.49 | $0.15 | $0.10 |
| JS rendering | $4.90 | $1.49 | $1.00 |
| Premium proxy + JS | $12.25 | $3.73 | $2.49 |
| Google SERP | $12.25 | $3.73 | $2.49 |
| Ultra premium + JS | $36.75 | $11.18 | $7.48 |

Two conclusions follow. Hobby is priced for testing, not for production: the same rendered page costs 4.9x what it costs on Startup. And anyone scraping Google or Amazon at volume should model the multiplier first, because a $149 plan buys 1,000,000 standard pages or 40,000 SERP requests, and the gap between those two numbers is where budgets break.

The free allowance is worth sizing the same way: 1,000 credits is 1,000 standard pages, 100 rendered pages, 40 Google SERPs, or 33 LinkedIn pages per month.

## What the headline price hides

Three mechanics matter more than the sticker price.

**There is no pay-as-you-go overage below Scaling.** When credits run out, scraping pauses until they renew. On Hobby, Startup, Business, Scaling and Professional you can switch on auto-upgrade, which moves you to the next plan the moment you run dry. Fixed-rate pay-as-you-go, capped at a monthly ceiling you set, only exists from Scaling upward. If you are on Startup and a crawl overshoots, the outcome is a stop or a bigger plan, not a small extra charge.

**Concurrency limits reject requests rather than bill them.** Go past your thread count and you get a 429 asking you to come back within the limit. There is no surcharge for the attempt, but the request is turned away instead of queued, so a crawler with poor backoff will show gaps rather than a bigger invoice.

**Country-level geotargeting starts at $299.** Free, Hobby and Startup cover US and EU only. If your project needs to see a product page as a shopper in Brazil or Japan, the cheapest plan that does it is Business.

👉 [Start the 7-day trial with 5,000 credits, no card required](https://www.scraperapi.com/pricing?fp_ref=coupons)

## How ScraperAPI compares on price per 1,000

Published entry prices are not comparable across these tools, because each one counts something different: credits, requests, records, results or Actor runs. The per-1,000 column is the useful one.

| Tool | Best for | Entry price | Cost signal per 1,000 | Parsing included | Main limit |
| --- | --- | --- | --- | --- | --- |
| ScraperAPI | Devs who keep their own parser and want fetch plus unblock | $49/mo (Hobby, 100K credits); free 1,000 credits | $0.15 standard, $1.49 rendered at Startup | No, apart from a few structured endpoints | No PAYG below Scaling; country targeting from $299 |
| Scrape.do | Cheapest base request rate | $29/mo for 250,000 requests | About $0.12 base, $0.58 rendered, $2.90 premium plus JS | No, but HTML, JSON, XML or markdown per request | Multipliers eat into the 250K base allowance |
| Zyte | Scrapy users and AI extraction | $5 trial credit for 30 days; PAYG $0.13/1K | $0.06 to $16.08 depending on target site difficulty | Partial, via AI extraction | Price is set by site difficulty, so budgets are hard to fix |
| Bright Data | Hard targets at enterprise scale | About $1.50/1K records; Micro $10/mo, Growth $499/mo | Around $1.50 per 1,000 records | No | Documentation and dashboard draw consistent user complaints |
| Firecrawl | LLM and RAG pipelines | Free 1,000 credits/mo, keyless trial; from $16/mo | Credit-based with feature multipliers | Yes, clean markdown, JSON or screenshot | Built for content, not per-field structured records |
| Apify | Ready-made scrapers you do not want to write | Free $5/mo credit; Starter $29/mo, Scale $199/mo | Varies per Actor | Yes, inside each Actor | Cost per Actor is hard to forecast before you run it |

Scrape.do is the sharper number for plain volume: $29 buys 250,000 requests, and a JavaScript-rendered page costs 5 credits there against 10 on ScraperAPI. Zyte is the wildcard, because the same monthly volume can land anywhere between $0.06 and $16.08 per 1,000 requests depending on how well defended the target is. Bright Data is a different purchase: you pay around $1.50 per 1,000 records for the success rate on sites that block lighter tools, and users consistently praise support while calling the documentation limited and the scraping interface overly complex.

## Who should not buy ScraperAPI

**You only need static HTML.** A `requests` call plus BeautifulSoup costs nothing, and if the pages are not defended you are paying $49 to $149 a month for a proxy you do not need.

**It is a one-off job of a few thousand pages.** The free tier covers 1,000 standard pages a month, and Firecrawl's keyless mode lets you test without an account at all. Neither requires a subscription decision.

**You already run a Scrapy pipeline and only lack IPs.** A raw proxy subscription is the cheaper fix. ScraperAPI's value is the browser and retry layer on top of the proxy, and you would be paying for plumbing you already built.

**Nobody on the team writes parsers.** ScraperAPI returns HTML. If you want records in a spreadsheet without code, a no-code tool such as Octoparse or Browse AI fits the job better, even though both cost more per page.

**You need city or ASN-level proxy control.** Geotargeting is country-level at best and only from Business up. Buy raw proxies if the target has to see a specific network.

## Picking a tier by workload

Under 1,000 pages a month, mostly static: stay on the free plan and spend nothing.

Testing whether a defended site can be scraped at all: use the 7-day trial's 5,000 credits. That is 5,000 standard pages, or 200 rendered ones.

100,000 to 1,000,000 credits a month of standard pages: Startup at $149. Hobby's per-credit rate makes it a stopgap at best.

Rendering or SERP work at real volume: Business at $299, which drops rendered pages to $1.00 per 1,000 and unlocks country targeting in the same purchase.

Occasional spikes past your allowance: you need Scaling or above for capped pay-as-you-go, so budget for that tier if bursts are part of the workload.

Feeding an LLM or a RAG index: confirm the output format before you buy anything. ScraperAPI returns raw HTML and leaves conversion to you; Firecrawl and Scrape.do both return markdown directly.

👉 [Compare the plans side by side before you commit](https://www.scraperapi.com/pricing?fp_ref=coupons)

## FAQ

**How much is one credit?** One standard page request. Harder targets and features cost more: Amazon 5, JS rendering 10, premium proxies 10, premium plus rendering 25, Google and Bing 25, LinkedIn 30, ultra premium with rendering 75. Every response reports its own cost in a header, and the dashboard has a per-URL cost estimator.

**Does JavaScript rendering cost extra?** Yes, 10 credits per request, and 25 when combined with premium proxies. If your targets are SPAs, multiply your expected page count by ten before choosing a plan.

**How long can I test for free?** Seven days with 5,000 credits and no card, then the free plan continues at 1,000 credits and 5 concurrent threads per month.

**Can I get raw HTML and parse it myself?** That is the intended workflow. Auto-parsing and output format changes are free, so you can request JSON where a structured endpoint exists and parse the HTML yourself everywhere else.

**What happens when credits run out?** Scraping pauses until they renew. Auto-upgrade moves you up a plan automatically on Hobby through Professional; capped pay-as-you-go is available from Scaling upward. Hitting your concurrency limit returns a 429 and the request is not charged.

**Is there a refund window?** ScraperAPI's public pages do not state one. Ask support before you take an annual plan, and start monthly while you are still measuring your credit burn.

## The short decision

Static pages and a few thousand requests: free tier, BeautifulSoup, done. Defended targets between 10,000 and a million pages a month with your own parser: Startup, moving to Business once rendering or country targeting enters the picture. Feeding an LLM: pick on output format first, since HTML costs you a conversion step that markdown does not.

Two things to confirm at checkout: the per-credit rate at the tier you are choosing, and whether your project needs geotargeting outside the US and EU. The second one silently doubles your minimum plan.

👉 [Check today's ScraperAPI plans and per-credit pricing](https://www.scraperapi.com/pricing?fp_ref=coupons)
