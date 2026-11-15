# DMIT Hosting: Which Plan Do You Actually Need, What It Costs per Year, and Do the Coupon Codes Still Work? (LAX, HKG and TYO Plan Tables)

DMIT's cheapest China-optimized entry point is **LAX.Pro.WEE at $36.9/year**: 1 vCPU, 1GB RAM, 500GB of traffic on a 500Mbps port, with three-carrier CN2 GIA return routing. Most readers should still think twice before buying it. It goes out of stock constantly, 1GB of RAM limits you to a static site, a proxy or a small WordPress install, and **$37.99/quarter for LAX.Pro.TINY** doubles both the RAM and the port speed.

Below: what the three network tiers actually mean, every plan currently listed in Los Angeles, Hong Kong and Tokyo, the annual cost math the plan tables hide, the policies that only surface after you pay, and whether the coupon codes still work.

> **Quick picks**
> - Cheapest way onto CN2 GIA: **LAX.Pro.WEE, $36.9/yr**
> - Best value for a site with Chinese visitors: **LAX.EB** (CMIN2 return) or **LAX.Pro.TINY, $37.99/quarter**
> - Lowest latency to mainland China: **HKG.Pro.MongKok, $149.9/yr**
> - Expecting attacks: **LAX.sPro** (Cloudflare Magic Transit on the inbound path, 5Tbps+ shared scrubbing, CN2 GIA still on the return)
> - Audience entirely in Europe or North America: DMIT is the wrong purchase

👉 [See every DMIT plan and what is currently in stock](https://www.dmit.io/aff.php?aff=9081)

## Pro, EB and T1: what the three tiers actually change

DMIT sells the same hardware behind three different routing profiles, and the price gap between them is entirely about how traffic reaches and leaves mainland China.

**Premium (Pro)** sends return traffic from all three Chinese carriers over CN2 GIA (AS4809). DMIT states publicly that the routing is not downgraded because of DDoS attacks or bandwidth cost, which matters more than the peak-hour numbers. Traffic is counted in both directions.

**Eyeball (EB)** keeps China Telecom and Unicom outbound on CN2 routes and China Mobile on CMIN2, with all three returning over CMIN2 or AS9929 load balancing. It is a real step down from Pro and still well above generic international transit. Billing counts both directions.

**Tier 1 (T1)** has no mainland China optimization at all. It is international transit, and traffic is counted **one way**: the larger of outbound and inbound. This is where newcomers lose money. A Hong Kong T1 box does not give you Hong Kong-to-mainland latency, because the packets are not routed toward the mainland at all. If your reason for buying is Chinese visitors, stay in Pro or EB.

One more variant worth knowing: **LAX.sPro (Premium Secure)** sends the inbound path through Cloudflare Magic Transit with 5Tbps+ of shared international DDoS scrubbing and keeps CN2 GIA on the return. One industry estimate puts the mainland-facing mitigation at around 100Gbps, which is a third-party guess rather than a published figure.

## Los Angeles plans

### LAX.Pro (three-carrier CN2 GIA return)

| Plan | vCPU / RAM / SSD | Traffic @ port | Price | Buy |
| --- | --- | --- | --- | --- |
| WEE | 1 / 1GB / 20GB | 500GB @ 500Mbps | **$36.9/yr** | [ Take the WEE annual plan](https://www.dmit.io/aff.php?aff=9081) |
| MALIBU | 1 / 1GB / 20GB | 1TB @ 1Gbps | $49.9/yr | [ Take the MALIBU annual plan](https://www.dmit.io/aff.php?aff=9081) |
| TINY | 1 / 2GB / 20GB | 1TB @ 1Gbps | **$37.99/quarter** | [ Start with the TINY quarterly](https://www.dmit.io/aff.php?aff=9081&pid=100) |
| Pocket | 2 / 2GB / 40GB | 1.5TB @ 4Gbps | $56.70/quarter | [ Take the Pocket quarterly](https://www.dmit.io/aff.php?aff=9081&pid=137) |
| STARTER | 2 / 2GB / 80GB | 3TB @ 10Gbps | $38.90/mo | [ Take the STARTER monthly](https://www.dmit.io/aff.php?aff=9081&pid=56) |
| MINI | 4 / 4GB / 80GB | 5TB @ 10Gbps | $76.90/mo | [ Take the MINI monthly](https://www.dmit.io/aff.php?aff=9081&pid=58) |
| MICRO | 4 / 4GB / 160GB | 7TB @ 10Gbps | $99.90/mo | [ Take the MICRO monthly](https://www.dmit.io/aff.php?aff=9081&pid=81) |
| MEDIUM | 6 / 8GB / 160GB | 15TB @ 10Gbps | $219.90/mo | [ Take the MEDIUM monthly](https://www.dmit.io/aff.php?aff=9081&pid=82) |
| LARGE | 8 / 16GB / 320GB | 25TB @ 10Gbps | see order page | [ Check LARGE pricing](https://www.dmit.io/aff.php?aff=9081&pid=61) |
| GIANT | 12 / 24GB / 640GB | 50TB @ 10Gbps | see order page | [ Check GIANT pricing](https://www.dmit.io/aff.php?aff=9081&pid=98) |

### LAX.EB (CMIN2 / AS9929 return)

| Plan | vCPU / RAM / SSD | Traffic @ port | Price | Buy |
| --- | --- | --- | --- | --- |
| WEE | 1 / 1GB / 20GB | 800GB–1TB @ 1Gbps | **$39.9/yr** | [ Take the EB WEE annual plan](https://www.dmit.io/aff.php?aff=9081) |
| TINY | 1 / 2GB / 20GB | 1.2–1.5TB @ 2Gbps | from ~$9.9/mo | [ Check the current EB TINY price](https://www.dmit.io/aff.php?aff=9081) |
| STARTER | 2 / 2GB / 40GB | 4TB @ 4Gbps | $29.90/mo | [ Take the EB STARTER monthly](https://www.dmit.io/aff.php?aff=9081) |
| MINI | 2 / 4GB / 80GB | 6TB @ 6Gbps | $49.90/mo | [ Take the EB MINI monthly](https://www.dmit.io/aff.php?aff=9081) |

### LAX.T1 (international only, one-way traffic)

| Plan | vCPU / RAM / SSD | Traffic @ port | Price | Buy |
| --- | --- | --- | --- | --- |
| TINY | 1 / 0.5GB / 10GB | 2000GB one-way @ 10Gbps | **$6.9/mo** | [ Take the T1 TINY monthly](https://www.dmit.io/aff.php?aff=9081) |
| STARTER | 1 / 1GB / 20GB | 4000GB one-way @ 10Gbps | $9.9/mo | [ Take the T1 STARTER monthly](https://www.dmit.io/aff.php?aff=9081) |
| MINI | 2 / 2GB / 40GB | 6000GB one-way @ 10Gbps | $16.9/mo | [ Take the T1 MINI monthly](https://www.dmit.io/aff.php?aff=9081) |

## Hong Kong and Tokyo plans

### HKG.Pro (CN2 GIA return)

| Plan | vCPU / RAM / SSD | Traffic @ port | Price | Buy |
| --- | --- | --- | --- | --- |
| MongKok | 1 / 1GB / 20GB | 200GB @ 150Mbps | **$149.9/yr** | [ Take MongKok, the cheapest HKG.Pro](https://www.dmit.io/aff.php?aff=9081) |
| Victoria | 1 / 2GB / 40GB | 500GB @ 300Mbps | $298.88/yr | [ Take Victoria](https://www.dmit.io/aff.php?aff=9081) |

### HKG.EB (CMI return)

| Plan | vCPU / RAM / SSD | Traffic @ port | Price | Buy |
| --- | --- | --- | --- | --- |
| STARTER | 1 / 1GB / 20GB | 500GB @ 500Mbps | **$6.9/mo** | [ Take the HKG.EB STARTER](https://www.dmit.io/aff.php?aff=9081) |
| MINI | 2 / 2GB / 40GB | 1000GB @ 1Gbps | $12.9/mo | [ Take the HKG.EB MINI](https://www.dmit.io/aff.php?aff=9081) |

### HKG.T1 and TYO.T1 (no mainland optimization)

| Plan | vCPU / RAM / SSD | Traffic @ port | Price | Buy |
| --- | --- | --- | --- | --- |
| HKG.T1 TINY | 1 / 0.5GB / 10GB | 2000GB @ 10Gbps | $3.9/mo | [ Take the HKG.T1 TINY](https://www.dmit.io/aff.php?aff=9081) |
| HKG.T1 STARTER | 1 / 1GB / 20GB | 4000GB @ 10Gbps | from $6.9/mo | [ Check the HKG.T1 STARTER price](https://www.dmit.io/aff.php?aff=9081) |
| TYO.T1 TINY | 1 / 0.5GB / 10GB | 2000GB @ 10Gbps | $3.9/mo | [ Take the TYO.T1 TINY](https://www.dmit.io/aff.php?aff=9081) |
| TYO.T1 STARTER | 1 / 1GB / 20GB | 4000GB @ 10Gbps | $6.9/mo | [ Take the TYO.T1 STARTER](https://www.dmit.io/aff.php?aff=9081) |

### TYO.Pro (CN2 GIA return)

| Plan | vCPU / RAM / SSD | Traffic @ port | Price | Buy |
| --- | --- | --- | --- | --- |
| STARTER | 1 / 1–1.5GB / 20GB | 500GB @ 100–500Mbps | from ~$32.9/quarter (annual billing discounted) | [ Check TYO.Pro STARTER availability](https://www.dmit.io/aff.php?aff=9081) |

A few rows above disagree between listings, and I would rather flag that than print one number as fact. The LARGE and GIANT prices in Los Angeles appear in three different forms across the sources, so the order page is the only figure worth trusting. EB TINY is listed at $9.9/mo, $9.99/mo and $17.90/mo in different places. The EB WEE has been described with both an 800GB and a 1TB quota, and the HKG.T1 STARTER with both 1GB and 1.5GB of RAM. TYO.Pro STARTER also shows three different configs. Nothing here is a discount you can rely on; check the cart before paying.

## What a year actually costs

The plan tables show whatever billing cycle each tier is priced in, which makes comparisons misleading. Converted to 12 months:

- **LAX.Pro.WEE**: $36.9/year, flat.
- **LAX.Pro.TINY**: $37.99 × 4 = **$151.96/year**. That is 4.1× the WEE price for 2GB instead of 1GB, 1TB instead of 500GB, and 1Gbps instead of 500Mbps.
- **LAX.EB.WEE**: $39.9/year, which is $3 more than Pro.WEE for CMIN2 return instead of CN2 GIA. If CN2 GIA is the reason you are on this page, paying extra to drop down a tier makes no sense. The EB WEE exists to catch people who search for "cheap DMIT plan" and stop at the first annual number.
- **LAX.T1.TINY**: $6.9 × 12 = **$82.8/year** for a plan with no China routing whatsoever. For roughly 45% of that you can have the Pro WEE with CN2 GIA, if you can catch it in stock.

The practical read: the WEE annual plans are loss leaders that sell out fast, the TINY quarterly is the cheapest plan that behaves like a normal server, and anything from STARTER upward is monthly billing for people running production traffic.

## The limits that show up after you pay

**Over-quota traffic gets throttled, not suspended.** Since 18 February 2025, LAX Pro and EB plans keep running after the monthly quota is exhausted and drop to a fixed speed instead. The tier depends on the plan: WEE and MALIBU-class plans fall to **2Mbps**, TINY, Pocket and STARTER to **4Mbps**, MINI and MICRO to **8Mbps**, MEDIUM and above to **10Mbps**. Some blog posts describe a 100Mbps–1Gbps throttle, which contradicts the published tiers, and one review claims Pro plans suspend on overage. Treat 2–10Mbps as the working assumption and size your traffic quota accordingly.

**Free IP replacement has four conditions.** A replacement costs nothing only if the instance was purchased at least 7 days ago, the last replacement (paid or free) was at least 15 days ago, both ICMP and all TCP ports are blocked, and the instance has at least 7 days of service left. Anything else is $5 per change, with requests no more often than every 7 days.

**Refunds.** Full refund inside 3 days if you have used 30GB or less. Inside 30 days you get a prorated refund based on remaining time or remaining traffic, minus the payment gateway fee. No refund if you have already refunded three instances in the same series, if the IP was hit by DDoS, if the reason is "network quality", if the IP is geolocated somewhere you dislike, if the IP is unreachable in a region but you have already pushed more than 3GB, or if you filed a chargeback.

**SSH keys only.** There is no password login option. The key pair is generated at checkout and you have to save the private key; lose it and you are reinstalling.

**No downgrades, no datacenter migration.** Upgrades cost the difference. Moving from Los Angeles to Hong Kong means buying a new server.

**No overselling means frequent stockouts.** Quotas are sold once and then the plan disappears from the store. This is also why the annual WEE plans are hard to catch.

👉 [Start with a quarterly LAX.Pro.TINY at $37.99 if you want to test the routing first](https://www.dmit.io/aff.php?aff=9081&pid=100)

## The coupon codes, and how much to trust them

Three codes circulate widely and appear in multiple sources:

- `LAX-EB-LAUNCH-NON-MONTHLY-RECURRING-20OFF` gives 20% recurring off LAX Eyeball on quarterly billing or longer.
- `2025-TYO-T1-HI-GSL-NON-MONTHLY-30OFF` gives 30% recurring off Tokyo T1 on quarterly billing or longer.
- `HKG-T1-ANNUALLY-45OFF-RECUR` gives 45% off Hong Kong T1 on annual billing, plus a configuration bump (more vCPU, double disk, 1.5× RAM).

Rules that apply to all of them: monthly billing usually does not qualify, the code has to be typed into the promo field at checkout and will not apply itself, and the first two still carry "2025" in their names, so validity is not guaranteed at the time you read this. Test the code in the cart before you pay. If it fails, the Promotions page in the client area lists whatever is currently running, and there are sometimes automatic discounts that need no code at all.

## When DMIT is the wrong choice

Skip it if any of these describe you. You only need a box for scripts, a bot or a monitoring probe, in which case a $3.9/month HKG.T1 TINY is overkill and a cheaper provider is fine. Your visitors are all in Europe or North America, where CN2 GIA buys you nothing. You want to downsize or move datacenters on a whim, which DMIT does not allow.

On the comparison that everyone asks about: BandwagonHost has purchased part of its CN2 GIA capacity from DMIT since 2021, which is a reasonable third-party signal about who actually controls the bandwidth. A third-party comparison puts a same-spec DMIT plan at roughly half the BandwagonHost price, with disk I/O measured at about 839MB/s versus 427MB/s, and notes that BandwagonHost's control panel is friendlier for beginners. Those figures come from review sites, not from DMIT.

The hardware behind the routing is current. DMIT moved the Los Angeles lineup to fourth-generation AMD EPYC 9654 hosts in October 2024, with free storage and traffic increases for existing customers, and some plans now sit on the newer EPYC 9005 platform. A third-party test of PVM.LAX.Pro.Pocket recorded a Geekbench 6 single-core score of 1728 and average disk throughput around 839MB/s. Peak-hour latency from mainland China to Los Angeles is reported at roughly 140–160ms with packet loss under 0.1%. Hong Kong numbers vary more between reviews, anywhere from 10–30ms to just under 50ms, so treat it as tens of milliseconds rather than a fixed figure.

## FAQ

**Can it run WordPress?** Yes on the 1GB plans, comfortably from 2GB upward. If you are serving Chinese visitors, put Cloudflare in front and you will survive traffic spikes on a TINY.

**Pro or EB?** Pro if you care about China Telecom and Unicom users at 9pm, or if a single bad routing week costs you money. EB if your traffic skews toward China Mobile or you are cost-sensitive. Either way, do not buy T1 expecting China optimization.

**Hong Kong or Los Angeles?** Hong Kong is for latency-critical mainland traffic and it costs several times more per unit of traffic. Los Angeles is the volume choice, and it also gives you a US IP for ad verification, streaming and AI service access that a Hong Kong IP will not.

**What happens if the IP gets blocked?** Pro-series IPs on premium routing are blocked less often than budget providers' IPs, but it happens. Check the four free-replacement conditions above before you open a ticket.

**Why is the plan I want out of stock?** Because DMIT does not oversell. The quota for that plan on that host is gone, so it is removed from the store until capacity appears.

## Final rules

- Under $40/year and you specifically want CN2 GIA → **LAX.Pro.WEE at $36.9/yr**, if it is in stock.
- A real server for a site with Chinese visitors → **LAX.Pro.TINY at $37.99/quarter**, or **LAX.EB.STARTER at $29.90/mo** if traffic volume matters more than routing grade.
- Latency is the product → **HKG.Pro.MongKok at $149.9/yr**, with **HKG.EB.STARTER at $6.9/mo** as the budget version.
- You expect to be attacked → **LAX.sPro**.
- International audience only → **LAX.T1.TINY at $6.9/mo**, and no China-specific expectation attached.

Before you pay, confirm two things: the billing cycle you selected actually meets the coupon's quarterly-or-longer threshold, and whether you need to tick **IP Guarantee+** so the IP is usable in the regions you care about. Then save the SSH private key from the client area.

👉 [Check current DMIT plan prices, stock and running promotions](https://www.dmit.io/aff.php?aff=9081)
