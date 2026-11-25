# ScraperAPI Pricing Calculator: What 100,000 Credits Actually Buys, Which Plan You Need, and Where the Real Costs Hide

ScraperAPI's cheapest paid plan costs $49 a month for 100,000 API credits, and those credits buy anywhere from roughly 1,300 to 100,000 page fetches depending on what you point them at. A plain HTML page costs 1 credit. An Amazon product page costs 5. A Google or Bing results page costs 25. A LinkedIn page costs 30. Any page where ScraperAPI has to defeat Cloudflare, DataDome or PerimeterX adds 10 credits on top.

That range is why a calculator built around team size produces a number you can't use. ScraperAPI bills on credits consumed, not seats: a 40-person team on Hobby pays $49, the same as one developer. What moves your bill is the mix of domains and feature flags in your workload. The tables and worked examples below let you price your own URL list before you commit to a tier.

> **Quick picks**
> - Mostly plain pages at moderate volume: Hobby, $49/mo for 100,000 credits.
> - Amazon, SERPs, or more than ~100K standard pages a month: Startup, $149/mo for 1,000,000 credits.
> - Geotargeting outside the US and EU: Business at $299/mo is the cheapest tier that offers it.
> - Unpredictable volume, or a mid-month cutoff would break your pipeline: Scaling at $475/mo, the first tier with pay-as-you-go.
> - Want to measure before you decide: 7-day trial, 5,000 credits, no credit card.

👉 See every plan and the current annual price

## All eight plans, with monthly and annual pricing

Annual billing takes a flat 10% off every paid tier. The annual column below shows the effective monthly rate when you pay for a year, not the total charged at checkout.

| Plan | Monthly | Annual (per month) | API credits/mo | Concurrent threads | Sign up |
| --- | --- | --- | --- | --- | --- |
| Free | $0 | n/a | 1,000 | 5 | [ Start free](https://www.scraperapi.com/signup?fp_ref=coupons) |
| Hobby | $49 | $44.10 | 100,000 | 20 | [ View plan](https://www.scraperapi.com/pricing?fp_ref=coupons) |
| Startup | $149 | $134.10 | 1,000,000 | 50 | [ View plan](https://www.scraperapi.com/pricing?fp_ref=coupons) |
| Business | $299 | $269.10 | 3,000,000 | 100 | [ View plan](https://www.scraperapi.com/pricing?fp_ref=coupons) |
| Scaling | $475 | $427.50 | 5,000,000 | 200 | [ View plan](https://www.scraperapi.com/pricing?fp_ref=coupons) |
| Professional | $975 | $877.50 | 10,500,000 | 300 | [ View plan](https://www.scraperapi.com/pricing?fp_ref=coupons) |
| Advanced | $1,975 | $1,777.50 | 21,500,000 | 500 | [ View plan](https://www.scraperapi.com/pricing?fp_ref=coupons) |
| Enterprise | Custom | Custom | 22,000,000+ | 500+ | [ Request a quote](https://www.scraperapi.com/contact-sales/?fp_ref=coupons) |

Every paid tier includes the same core feature set: JS rendering, premium residential and mobile IPs, anti-bot bypass, JSON autoparse, rotating proxy pools, custom headers, CAPTCHA handling, desktop and mobile user agents, automatic retries, unlimited bandwidth, a 99.9% uptime guarantee and full crawler access. The tiers differ on credits, concurrency and the items in this second table.

| Plan | Geotargeting | Analytics history | Pay-as-you-go | Support |
| --- | --- | --- | --- | --- |
| Free | Not listed | Not listed | No | Standard |
| Hobby | US and EU only | 30 days | No | Standard |
| Startup | US and EU only | 30 days | No | Standard |
| Business | Global, country level | Unlimited | No | Standard |
| Scaling | Global, country level | Unlimited | Yes | Standard |
| Professional | Global, country level | Unlimited | Yes | Priority support |
| Advanced | Global, country level | Unlimited | Yes | Priority routing |
| Enterprise | Global, country level | Unlimited | Yes | Dedicated team, Slack |

There is no seat count anywhere in those tables. Some third-party calculators ask for team size and multiply the plan price, which produces an inflated total; the list price is flat no matter how many people share the API key. Adding users costs nothing. Adding credits costs money.

## How the credit multiplier works, with two worked examples

Credits are priced per request by target domain, and the multiplier is fixed per domain rather than per plan. Upgrading lowers what you pay for a credit, never how many credits a request consumes.

| Target | Credits per request |
| --- | --- |
| Standard page | 1 |
| Amazon, including all regional domains | 5 |
| Google and Bing, including subdomains | 25 |
| LinkedIn | 30 |
| Pages behind Cloudflare, DataDome or PerimeterX | +10 on the base cost |

Run the arithmetic on your own mix before picking a tier. On Hobby, 100,000 credits divided by 5 credits per Amazon request gives you 20,000 Amazon product pages a month. The same workload on Scaling's 5,000,000 credits reaches 1,000,000 pages. A standard page sitting behind Cloudflare costs 1 + 10 = 11 credits, so Hobby covers about 9,090 of those. The bypass surcharge is applied automatically when ScraperAPI activates its bypass logic, not when you ask for it.

Feature flags add their own credits on top of the domain category. ScraperAPI's credit cost documentation lists a plain request at 1 credit, JS rendering at 10, a premium proxy at 10, premium plus JS rendering at 20, ultra_premium at 30, and ultra_premium plus JS rendering at 75. Those numbers are already combined totals across the category and the flags, and the same table gives higher figures for e-commerce and SERP targets. At 75 credits a request, Hobby's 100,000 credits cover roughly 1,333 fetches. The same $49 buys 100,000 plain requests or 1,333 heavily protected rendered ones, which is a 75x swing in capacity for an unchanged invoice.

Two tools in the dashboard keep this from being guesswork. The Domain Cost Estimator returns the exact credit cost for any URL before you run it, and a `max_cost` parameter caps the spend on any single request. If your targets are an awkward mix, price twenty representative URLs through the estimator rather than trusting a category average.

👉 Start a 7-day trial with 5,000 credits and cost your own URLs

## The per-credit price curve flattens after Business

ScraperAPI doesn't publish a per-credit rate, so here it is calculated from list prices. Divide the monthly price by the credit allowance.

| Plan | Monthly | Credits | Cost per 1,000 credits |
| --- | --- | --- | --- |
| Hobby | $49 | 100,000 | $0.49 |
| Startup | $149 | 1,000,000 | $0.149 |
| Business | $299 | 3,000,000 | ~$0.0997 |
| Scaling | $475 | 5,000,000 | $0.095 |
| Professional | $975 | 10,500,000 | ~$0.0929 |
| Advanced | $1,975 | 21,500,000 | ~$0.0919 |

Going from Hobby to Startup cuts your unit cost by about 70%, and Startup to Business cuts it by another third. After Business the curve goes flat: moving from $299 to $1,975 a month, a 6.6x increase in spend, improves the per-credit price by only about 8%.

That matters when you're choosing between the top tiers. Scaling, Professional and Advanced are not better rates in any meaningful sense. They are bigger credit buckets with more concurrency, running from 200 threads at Scaling to 500 at Advanced, and pay-as-you-go headroom. If you're looking at Advanced because you assume the unit economics improve, you're buying throughput, not a discount.

## Three limits that decide your plan more than monthly volume

**Credits reset every billing cycle.** Unused credits are lost at renewal, not carried forward. A workload that swings between 400,000 and 900,000 pages a month has to be sized for the peak, because the quiet month's surplus evaporates. There is also no proactive alert when you're burning through an allowance; you watch usage in the dashboard.

**Pay-as-you-go starts at Scaling.** Hobby, Startup and Business have no overflow option. Hit the limit mid-month on those tiers and requests are refused until renewal, unless you've enabled auto-upgrade to move up a tier automatically. Auto-upgrade is opt-in and available on Hobby, Startup, Business, Scaling and Professional. PAYG is the other mechanism: it keeps you on your current plan and bills extra credits at a fixed rate, capped at a monthly spending limit you set in the dashboard.

**Global geotargeting starts at Business.** Hobby and Startup target the US and EU only. If any part of your workload needs to appear to come from Brazil, Japan or India, $299/mo is the entry point, and there is no add-on or workaround on the lower tiers. Geotargeting is country level, not city level, on every plan.

Those three together explain most of the upgrade decisions I'd expect from a ScraperAPI customer: not "my volume doubled" but "my volume doubled in a month I hadn't planned for" or "we expanded past the US."

## What happens when you exceed a limit

Requests beyond your concurrency limit or your credit allowance come back as a 429 response. The request is refused, not queued, and there is no overage charge for hitting the ceiling. Reduce concurrency and retry, or wait for renewal.

The three ways to avoid the wall do different things, and ScraperAPI's own FAQ separates them:

- **Upgrading** moves you to a higher tier with a larger allowance and usually a better price per credit. You can do it from the billing page at any time, up or down.
- **Auto-upgrade** performs that move automatically when credits run out. It's opt-in, and it's available on Hobby, Startup, Business, Scaling and Professional.
- **Pay-as-you-go** keeps the plan unchanged and bills extra credits at a fixed per-credit rate, capped at a limit you set. It's available on Scaling, Professional, Advanced and Enterprise.

Annual plans can also be renewed early to get a fresh batch of credits, which is a cheaper reset than upgrading if you've simply front-loaded a project.

👉 Compare the tiers that include pay-as-you-go

## When ScraperAPI is the wrong purchase

If your scraping is a few thousand plain HTML pages a month, the free plan's 1,000 credits and 5 concurrent connections may cover your testing, and Hobby covers the rest. Buying Business for credits you won't consume gets you a bigger concurrency allowance and global geotargeting you don't need.

Workloads dominated by JavaScript rendering are the other case worth flagging. Third-party comparisons of the two tools argue that ScrapingBee is more economical when most of your requests need rendering, because ScraperAPI charges rendering as credits on top of the domain category. For sites with heavy protection, where you'd stack premium proxies and rendering and land at 75 credits a request, Bright Data's Web Unlocker bills a flat rate per request instead of multiplying, which makes monthly cost easier to predict.

ScraperAPI also isn't a platform. The core product is one API endpoint: you send a URL, it routes the request through its proxy pool and returns HTML, with rendering and CAPTCHA handling as options. Scheduling, storage, prebuilt crawlers and workflow automation are yours to build, with the exception of DataPipeline for scheduled jobs. One thing to note if you're budgeting from older write-ups: ScraperAPI's documentation now states that DataPipeline credit costs match its standard scraping rates, so the separate, higher DataPipeline schedule that appeared in earlier reviews (a flat page at 6 credits) no longer applies.

## FAQ

**Is one credit always one request?**
No. A standard page is 1 credit, Amazon is 5, Google and Bing are 25, LinkedIn is 30, and anti-bot bypass adds 10. Rendering and proxy flags add more.

**Do unused credits roll over?**
No. The balance resets on each renewal date.

**Can I pay monthly?**
Yes, every tier offers monthly and annual billing, and annual is 10% cheaper. There are no longer commitments beyond the billing period you pick.

**What happens if I go over my limit?**
You get a 429 response, the request is refused rather than queued, and you aren't charged extra. Auto-upgrade or pay-as-you-go are the two ways to avoid the cutoff.

**Is there a refund?**
Yes. ScraperAPI offers a 7-day, no-questions-asked refund; contact support and the charge is reversed. Cancelling is free and can be done from the dashboard at any time.

**Does adding team members cost more?**
No. Plan pricing is per account, not per seat, and everyone sharing the API key runs against the same credit pool and concurrency limit.

## How to choose in one pass

Match the plan to the constraint that binds first, not to the biggest number on the page:

- Plain pages, under ~100,000 a month: Hobby at $49.
- Amazon or moderate SERP volume, or anything up to ~1,000,000 standard pages: Startup at $149.
- Need to appear to come from outside the US and EU: Business at $299, no alternative.
- Can't tolerate a mid-month cutoff: Scaling at $475 for pay-as-you-go.
- Need 22M+ credits or a negotiated rate: Enterprise, quoted through sales.

Two things to confirm before you enter a card. First, whether any part of your workload targets a country outside the US and EU, because that single requirement moves your floor from $149 to $299. Second, whether being cut off mid-month is survivable, because on Hobby, Startup and Business it isn't optional without auto-upgrade.

If either answer is uncertain, the trial settles it: 7 days and 5,000 credits with no card, plus a 7-day refund window on the first paid month if the real numbers come in worse than the estimate.

👉 Check current pricing and start with the 7-day trial
