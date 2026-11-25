# Scrapingdog vs ScraperAPI: which is cheaper on your targets, which plan covers your volume, and where the credit rules add to the bill (full ScraperAPI plan table included)

On sticker price, Scrapingdog is the cheaper of the two. Entry plans are $40 a month for 200,000 credits against $49 for 100,000, and a million credits costs $90 against $149. Whether that gap survives contact with your actual workload is a different question, because the two services price difficulty very differently: an Amazon page costs 1 credit on Scrapingdog and 5 on ScraperAPI, a Google SERP costs 5 against 25, and JavaScript rendering costs 5 against 10.

Below are both multiplier tables, all eight ScraperAPI plans, the cost of 1,000 pages on three common targets with the arithmetic shown, and the billing rules that decide whether your budget holds.

> **Quick answer.** Test your own URLs before you pick a tier. ScraperAPI's 7-day trial gives 5,000 credits with no card, which at its own rates is 5,000 plain pages, 1,000 Amazon pages, 500 rendered pages or 200 Google SERPs, enough to see whether your targets return at all.
>
> 👉 [Start the 7-day trial with 5,000 credits](https://www.scraperapi.com/?fp_ref=coupons)

## ScraperAPI plans and prices in full

ScraperAPI sells eight tiers plus a free allowance, and every paid tier ships the same core feature set: JS rendering, premium proxies, JSON auto-parsing, CAPTCHA handling and a 99.9% uptime commitment. What changes between tiers is volume, concurrency and how precisely you can geotarget.

| Plan | Price (monthly / annual per month) | API credits | Threads | Geotargeting | Get started |
| --- | --- | --- | --- | --- | --- |
| Free | $0 | 1,000 / month | 5 | — | [ Create a free account](https://www.scraperapi.com/?fp_ref=coupons) |
| Free Trial | $0 for 7 days | 5,000 | 5 | — | [ Run the 7-day trial](https://www.scraperapi.com/?fp_ref=coupons) |
| Hobby | $49 / $44.10 | 100,000 | 20 | US & EU | [ Get the Hobby plan](https://www.scraperapi.com/?fp_ref=coupons) |
| Startup | $149 / $134.10 | 1,000,000 | 50 | US & EU | [ Get the Startup plan](https://www.scraperapi.com/?fp_ref=coupons) |
| Business | $299 / $269.10 | 3,000,000 | 100 | Country-level | [ Get the Business plan](https://www.scraperapi.com/?fp_ref=coupons) |
| Scaling (most popular) | $475 / $427.50 | 5,000,000 | 200 | Country-level | [ Get the Scaling plan](https://www.scraperapi.com/?fp_ref=coupons) |
| Professional | $975 / $877.50 | 10,500,000 | 300 | Country-level | [ Get the Professional plan](https://www.scraperapi.com/?fp_ref=coupons) |
| Advanced | $1,975 / $1,777.50 | 21,500,000 | 500 | Country-level | [ Get the Advanced plan](https://www.scraperapi.com/?fp_ref=coupons) |
| Enterprise | Custom | 22,000,000+ | 500+ | Country-level | [ Talk to sales](https://www.scraperapi.com/?fp_ref=coupons) |

Three rules under that table change what you actually pay:

- **Annual billing takes 10% off every paid tier.** Hobby drops to $44.10 a month, Startup to $134.10, Business to $269.10. The discount is applied to the same credit allowance, not a smaller one.
- **Credits reset at renewal and do not roll over.** A light month is not banked for a heavy one, so pick the tier for your peak month, not your average.
- **Overage is gated.** Pay-as-you-go spillover at a fixed per-credit rate exists on Scaling, Professional, Advanced and Enterprise. On Hobby through Professional you can instead opt into auto-upgrade, which moves you to the next tier when credits run out; without either, scraping pauses until the cycle renews. That detail matters more than the headline price if your traffic is spiky.

## The credit multiplier is where the price gap actually lives

ScraperAPI moved from flat per-call billing to difficulty-weighted credits in 2022, and that change is the source of most "my credits vanished faster than expected" complaints in reviews. The multipliers are published, and they do most of the work in this comparison.

| Request type | ScraperAPI | Scrapingdog |
| --- | --- | --- |
| Standard page | 1 credit | 1 credit |
| JavaScript rendering | 10 credits | 5 credits |
| Amazon (structured endpoint vs dedicated API) | 5 credits | 1 credit |
| Google SERP | 25 credits (Google and Bing, subdomains included) | 5 credits (SERP Light), 10 (Advance) |
| LinkedIn | 30 credits via standard endpoint | 50 credits via profile scraper |
| Premium proxy | +10 credits | 10 credits |
| JS rendering + premium proxy | 25 credits | 25 credits |
| Bot-protection bypass (Cloudflare, DataDome, PerimeterX) | +10 credits | included |
| Screenshot | 10 credits | 5 credits |
| Ultra premium / ultra premium + JS | 30 / 75 credits | not offered |

LinkedIn is the one row where ScraperAPI is the cheaper option per request, which is worth knowing if LinkedIn is a big part of your pipeline. For nearly everything else, the multiplier gap runs against it.

## What 1,000 pages actually cost on each

The formula is simple: price per credit multiplied by credits per request, then multiplied by 1,000. Comparing the two services at the 1,000,000-credit tier, ScraperAPI Startup costs $0.000149 per credit and Scrapingdog Standard costs $0.00009.

| Target | ScraperAPI (Startup, $149/1M) | Scrapingdog (Standard, $90/1M) |
| --- | --- | --- |
| Plain HTML page | 1 credit → **$0.15** per 1,000 | 1 credit → **$0.09** per 1,000 |
| JS-rendered page | 10 credits → **$1.49** | 5 credits → **$0.45** |
| Amazon product or search | 5 credits → **$0.75** | 1 credit → **$0.09** |
| Google SERP | 25 credits → **$3.73** | 5 credits → **$1.00** |

At the entry tiers the spread widens, because the price per credit is worse on both sides. ScraperAPI Hobby is $0.49 per 1,000 credits, so a rendered page costs $4.90 per 1,000 and a Google SERP costs $12.25. Scrapingdog Lite is $0.20 per 1,000 credits, so the same rendered page costs $1.00 and an Amazon page costs $0.20.

Read those numbers as a workload profile rather than a verdict. If you scrape 200,000 Amazon pages a month, ScraperAPI Startup bills roughly $150 in credits for work that fits inside Scrapingdog's $90 Standard plan. If you scrape long-tail domains with no dedicated endpoint, both charge 1 credit a page, and the comparison collapses to $149 against $90 for the same million pages, with ScraperAPI's larger proxy pool and concurrency as the tiebreaker.

One caveat on all of the above: these are estimates from published multipliers. They exclude retries, pages that return 404, and duplicate requests caused by caching.

## Speed and success rates: what the published benchmark can and cannot tell you

The most-cited speed comparison in this category comes from Scrapingdog's own blog, published in January 2026, using one Python script and 10 requests per site.

| Target | ScraperAPI average / success | Scrapingdog average / success |
| --- | --- | --- |
| Amazon | 40.65s / 100% | 5.48s / 100% |
| Glassdoor | 20.48s / 100% | 5.57s / 100% |
| eBay | 8.28s / 100% | 5.91s / 100% |
| Walmart | 18.89s / 100% | 4.48s / 100% |
| Google SERP | 27.25s / 80% | 1.25s / 100% |

Those figures get republished widely, sometimes as "independent tests". They are not independent: the vendor selling one of the two products ran the test, published the code, and did not disclose the time window or the region the requests came from. Ten requests per site is also a small sample. Both of those caveats come from people who compare scraping APIs for a living, and the general guidance is that any vendor-run benchmark deserves a discount.

Success-rate claims conflict in the same way. ScraperAPI's own comparison page advertises 99.99% success; Scrapingdog's page claims 99%+ on top-level domains while putting ScraperAPI near 85%; third-party write-ups note that both services return 0% on some social platforms. Every one of those numbers comes from a party with an interest in the outcome. Treat all of them as marketing until your own target list says otherwise.

That is the practical argument for testing rather than trusting a table: 5,000 credits will tell you more about your five hardest URLs than any published average.

👉 [Put the 5,000 trial credits against your own URL list](https://www.scraperapi.com/?fp_ref=coupons)

## Feature differences that decide the purchase

|  | ScraperAPI | Scrapingdog |
| --- | --- | --- |
| Geotargeting from the entry paid tier | US & EU only until Business ($299) | 15 countries from Lite ($40) |
| Concurrency, entry paid tier | 20 threads | 5 threads |
| Dedicated / structured endpoints | 18 structured endpoints (Amazon, Google, Walmart, eBay, Redfin) | dedicated APIs for Google SERP, AI Mode, Maps, Trends, LinkedIn, Twitter, TikTok, YouTube, Amazon, Walmart, Flipkart, eBay |
| Scheduled no-code jobs | DataPipeline, up to 10,000 URLs per project, billed in extra credits | not a core listed feature |
| LLM-ready output | `output_format` returns Text or Markdown | not available |
| Proxy types | datacenter, residential, mobile | datacenter and residential |
| Failed requests | non-200/404 responses not billed; 404s still consume credits | failed requests credited back |
| Refund policy | 7-day, no questions asked | not listed on the pricing page |

Both companies publish proxy-pool numbers that differ between their own marketing pages and third-party write-ups (ScraperAPI is quoted at 40M+ IPs and 50+ countries in one place and 150M+ IPs across 150+ countries in another; Scrapingdog at 10M+ IPs and 15 countries). Treat pool size as directional and test the domains you care about.

The two features that genuinely separate them are geotargeting and the dedicated endpoints. Country-level targeting on ScraperAPI starts at $299 a month. On Scrapingdog it starts at $40. If your project needs to see localized prices or search results in a specific country, that single line item is worth $259 a month.

## Where Scrapingdog is the better buy

Four situations where the cheaper option is also the right one:

- **Your targets are concentrated on Google SERP, Amazon or JavaScript-heavy pages.** At 5 credits against 25 for SERP and 1 against 5 for Amazon, the effective cost difference runs from roughly 3x to 8x on the same volume. No amount of proxy-pool size compensates for that if those are your only targets.
- **You need 15-country geotargeting and cannot justify $299 a month.** Lite at $40 covers it.
- **You want a very fine-grained ladder.** Scrapingdog sells 27 plans from $40 up to a $30,000 Nova Pro tier, which lets you step up in small increments instead of jumping from $299 to $475.
- **You need dedicated endpoints for LinkedIn, TikTok, YouTube or Indeed.** ScraperAPI routes LinkedIn through a standard endpoint at 30 credits and is not a reliable option on several social platforms.

The trade-offs are real too: 5 concurrent threads on the entry plan is a prototyping budget, there is no pay-as-you-go spillover inside a subscription (overage credits are bought separately and cannot be combined with your plan), and failed requests are refunded but the pricing page does not state a refund window for the subscription itself.

## Five ways this comparison gets more expensive than the sticker price

1. **A 404 still costs credits.** On ScraperAPI, a page that returns 404 consumes credits even though you got nothing; other non-200 outcomes are not billed. Crawling a large site with dead URLs quietly eats into your allowance.
2. **The hardest targets are cached for up to 10 minutes.** If you monitor prices or stock levels, you may be reading data that is up to 10 minutes old, and polling faster than that just burns credits for the same cached page.
3. **Nothing rolls over.** Credits reset at renewal on both services. Buying a tier above your real monthly volume to "bank" capacity does not work.
4. **Geotargeting is locked behind Business.** Country-level targeting on ScraperAPI means $299 a month, which is $150 more than Startup and $259 more than Scrapingdog's Lite. Budget for it before you compare plans, not after.
5. **Overage rules are asymmetric.** ScraperAPI's pay-as-you-go only opens at Scaling ($475); below that, auto-upgrade is the only way to keep running mid-cycle, and it moves you to the next tier's price. Scrapingdog's overage credits are a separate purchase that does not combine with your subscription.

## FAQ

**Which one is cheaper?**
On list price and on most per-page workloads, Scrapingdog: $40 against $49 at entry, $90 against $149 for a million credits, and 5 against 10 credits for rendering. ScraperAPI is cheaper per request on LinkedIn and cheaper per successful page when your targets are long-tail domains where Scrapingdog's dedicated APIs give no advantage.

**Does 1 million credits mean 1 million requests?**
No. On ScraperAPI, 1,000,000 credits is 1,000,000 plain pages, 200,000 rendered pages, 200,000 Amazon pages or 40,000 Google SERPs. On Scrapingdog at the same tier, it is 1,000,000 plain pages, 200,000 rendered pages, 1,000,000 Amazon pages or 200,000 SERP requests. Model your real mix before choosing a tier.

**I mostly scrape Amazon and Google SERP. Which should I pick?**
Scrapingdog on cost, by a wide margin at these multipliers. Run a small batch through both before committing if uptime matters more than price, since the published success rates for Amazon are 100% for both in the only public benchmark.

**Can I get a refund?**
ScraperAPI states a 7-day, no-questions-asked refund. Scrapingdog does not list a refund policy on its pricing page, so ask support before paying for an annual plan.

**Is the free allowance enough to test?**
For ScraperAPI, 5,000 trial credits is 5,000 plain pages, 1,000 Amazon pages, 500 rendered pages or 200 SERPs, which is enough for a real pilot on a narrow target list. After the trial the free plan continues at 1,000 credits a month with 5 threads.
👉 [Claim the trial and size your workload from real data](https://www.scraperapi.com/?fp_ref=coupons)

**What does a small team buy first?**
ScraperAPI Hobby at $49 covers 100,000 credits, which is 20,000 Amazon pages, 10,000 rendered pages or 4,000 Google SERPs a month at 20 concurrent threads. Move to Startup at $149 only when you are consistently hitting that ceiling, since it triples the credit allowance and more than doubles the concurrency.
👉 [Compare what Hobby and Startup include](https://www.scraperapi.com/?fp_ref=coupons)

## How to decide

Match the plan to the workload, not to the brand:

- **Amazon, Google SERP or JS-heavy pages at volume, on a tight budget** → Scrapingdog, and accept 5 threads at entry level.
- **Mixed long-tail domains where success rate matters more than unit cost, and you want a documented 7-day refund** → ScraperAPI, starting at Hobby and moving to Startup once you pass 100,000 credits.
- **Country-level geotargeting on a small budget** → Scrapingdog Lite at $40; on ScraperAPI the same capability starts at $299.
- **Recurring scheduled jobs, Markdown output for LLM pipelines, or mobile proxies** → ScraperAPI, since DataPipeline, `output_format` and mobile IPs are not offered on the other side.

Before you enter a card number, confirm two things on the live page: that the plan prices and credit allowances above still match what ScraperAPI displays, since allowances and bonus credits change, and that the trial terms (7 days, 5,000 credits, no card) and the 7-day refund window are still in force.

👉 [Check the current ScraperAPI plans and start the free trial](https://www.scraperapi.com/?fp_ref=coupons)
