# best cn2 gia vps: BandwagonHost Plans, Pricing, Latency & How to Pick the Right One for China Traffic

If you've ever tried serving content into Mainland China from a generic overseas VPS, you already know what happens around 8 PM: latency doubles, packet loss climbs past 20–30%, video calls freeze, and SSH sessions stutter. That's not a VPS problem — it's a transit problem. Most cheap providers ship traffic over AS4134 (ChinaNet/163), the cheapest and most congested path into China. CN2 GIA exists precisely to fix that.

This guide walks through what CN2 GIA actually is, why BandwagonHost has become the default name people land on when searching for it, how the different plan families compare on price and latency, and which one is likely the right fit for your workload.

## What CN2 GIA Is (And Why It Costs More)

China Telecom runs four tiers of IP transit, and the differences matter more than marketing would suggest:

- **AS4134 (ChinaNet/163)** — the cheapest, highest-capacity route, and the one most cloud providers default to. Fine for absorbing large DDoS attacks because of its raw capacity, bad for anything latency-sensitive during peak hours.
- **AS4809 CN2 GT (Global Transit)** — originally pitched as the fix for 163 congestion. Since 2019 it has slipped back toward similar peak-hour problems despite costing more.
- **AS4809 CN2 GIA (Global Internet Access)** — the premium tier. Stable, low packet loss, the network you want for VoIP, web conferencing, online gaming, and serving content to Chinese users. The catch: capacity is limited and per-megabit costs can run extremely high — BandwagonHost notes CN2 GIA IP transit can hit around $120 per megabit in some markets.
- **AS23764 CTGNet** — China Telecom's newest option, effectively equivalent to CN2 GIA in performance and price.

BandwagonHost operates CN2 GIA / CTGNet links out of Los Angeles (DC9 / USCA_9), Hong Kong, Tokyo, Osaka, and Singapore. On the Los Angeles eCommerce plans, China-bound traffic is split across CN2 GIA (AS4809), CMIN2 (China Mobile AS58807), and China Unicom Premium (AS10099) — the "tri-network" routing you'll see referenced in third-party reviews.

The short version: CN2 GIA is the most expensive way to move data in and out of China, and it's also the most stable. That combination explains why plans built on it cost more than generic KVM VPS lines.

## CN2 GIA vs CN2 GIA-E: Two Different Products

This is the single most common point of confusion, so it's worth clearing up directly.

**CN2 GIA** refers to the network tier. BandwagonHost applies that label to its dedicated Hong Kong, Tokyo, Osaka, and Singapore lines — physically locked to one city, premium latency, premium price. Hong Kong CN2 GIA typically lands at 30–60 ms from major Chinese cities; Tokyo sits around 40–80 ms.

**CN2 GIA-E** (the "E" stands for E-Commerce) is a separate product family based in Los Angeles. It rides the same CN2 GIA backbone on the China-bound leg, but adds CMIN2 and China Unicom Premium routing, supports 2.5–10 Gbps port speeds (versus the 1–1.5 Gbps on most Asia CN2 GIA plans), and lets you migrate the VPS between 11+ datacenters for free. That flexibility is why most reviewers point new buyers here as the default starting point.

In practice: if absolute lowest latency matters more than money, pick Hong Kong or Tokyo CN2 GIA. If you want the best balance of price, bandwidth, and route flexibility, CN2 GIA-E out of Los Angeles is the sensible default.

## BandwagonHost CN2 GIA-E Plans (Los Angeles)

This is the family most buyers end up in. 2.5–10 Gbps ports, 11+ migratable datacenters including DC6 CN2 GIA-E, DC9 CN2 GIA, JPOS_1 (Japan SoftBank), EUNL_9 (Netherlands CN2), plus the standard DC2/DC4/DC8/FMT/USNJ/USNY/EUNL/CABC pool.

| Plan | CPU | RAM | Storage | Transfer | Port | Billing | Order |
| --- | --- | --- | --- | --- | --- | --- | --- |
| CN2 GIA-E 1GB | 2 cores | 1 GB | 20 GB SSD | 1 TB/mo | 2.5 Gbps | $49.99/qtr · $169.99/yr | [ Order CN2 GIA-E 1GB](https://bwh81.net/aff.php?aff=77528&pid=87) |
| CN2 GIA-E 2GB | 3 cores | 2 GB | 40 GB SSD | 2 TB/mo | 2.5 Gbps | $89.99/qtr · $299.99/yr | [ Order CN2 GIA-E 2GB](https://bwh81.net/aff.php?aff=77528&pid=88) |
| CN2 GIA-E 4GB | 4 cores | 4 GB | 80 GB SSD | 3 TB/mo | 2.5 Gbps | $56.99/mo · $549.99/yr | [ Order CN2 GIA-E 4GB](https://bwh81.net/aff.php?aff=77528&pid=89) |
| CN2 GIA-E 8GB | 6 cores | 8 GB | 160 GB SSD | 5 TB/mo | 5 Gbps | $86.99/mo · $879.99/yr | [ Order CN2 GIA-E 8GB](https://bwh81.net/aff.php?aff=77528&pid=90) |
| CN2 GIA-E 16GB | 8 cores | 16 GB | 320 GB SSD | 8 TB/mo | 5 Gbps | $159.99/mo · $1599.99/yr | [ Order CN2 GIA-E 16GB](https://bwh81.net/aff.php?aff=77528&pid=91) |
| CN2 GIA-E 32GB | 10 cores | 32 GB | 640 GB SSD | 10 TB/mo | 10 Gbps | $289.99/mo · $2759.99/yr | [ Order CN2 GIA-E 32GB](https://bwh81.net/aff.php?aff=77528&pid=92) |
| CN2 GIA-E 64GB | 12 cores | 64 GB | 1 TB SSD | 12 TB/mo | 10 Gbps | $549.99/mo · $5399.99/yr | [ Order CN2 GIA-E 64GB](https://bwh81.net/aff.php?aff=77528&pid=93) |

The $49.99/quarter entry point is the most-bought plan in the entire catalog — enough RAM and transfer for a personal proxy, a small site, or a build box, with full CN2 GIA-E routing. Annual billing consistently works out cheaper per month across every tier.

## Hong Kong CN2 GIA — The Lowest-Latency Option

Hong Kong is the lowest-latency option in the catalog, typically 30–60 ms from major Chinese metros. The trade-off is price and a 1 Gbps port cap. Hong Kong plans can be migrated to other Asia CN2 GIA locations (Tokyo, Osaka, Singapore) free of charge.

| Plan | CPU | RAM | Storage | Transfer | Port | Billing | Order |
| --- | --- | --- | --- | --- | --- | --- | --- |
| HK CN2 GIA 2GB | 2 cores | 2 GB | 40 GB SSD | 500 GB/mo | 1 Gbps | $89.99/mo · $899.99/yr | [ Order HK 2GB](https://bwh81.net/aff.php?aff=77528&pid=95) |
| HK CN2 GIA 4GB | 4 cores | 4 GB | 80 GB SSD | 1 TB/mo | 1 Gbps | $155.99/mo · $1559.99/yr | [ Order HK 4GB](https://bwh81.net/aff.php?aff=77528&pid=96) |
| HK CN2 GIA 8GB | 6 cores | 8 GB | 160 GB SSD | 2 TB/mo | 1 Gbps | $299.99/mo · $2999.99/yr | [ Order HK 8GB](https://bwh81.net/aff.php?aff=77528&pid=97) |
| HK CN2 GIA 16GB | 8 cores | 16 GB | 320 GB SSD | 4 TB/mo | 1 Gbps | $589.99/mo · $5899.99/yr | [ Order HK 16GB](https://bwh81.net/aff.php?aff=77528&pid=98) |
| HK CN2 GIA 32GB | 10 cores | 32 GB | 640 GB SSD | 6 TB/mo | 1 Gbps | $989.99/mo · $9989.99/yr | [ Order HK 32GB](https://bwh81.net/aff.php?aff=77528&pid=122) |
| HK CN2 GIA 64GB | 12 cores | 64 GB | 1 TB SSD | 8 TB/mo | 1 Gbps | $1889.99/mo · $18989.99/yr | [ Order HK 64GB](https://bwh81.net/aff.php?aff=77528&pid=124) |

If your workload is interactive — gaming, remote desktop, real-time trading, anything where 150 ms of extra RTT hurts — Hong Kong is hard to beat. The 1 Gbps port is the main thing that holds it back for bandwidth-heavy use cases.

## Tokyo CN2 GIA — Low Latency With a Slightly Larger Port

Tokyo plans share the same CPU/RAM/storage layout as Hong Kong but bump the port to 1.2 Gbps. Latency from China lands around 40–80 ms. Tokyo is the right pick when Hong Kong is out of stock or when you specifically want Japan-side peering.

| Plan | CPU | RAM | Storage | Transfer | Port | Billing | Order |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Tokyo CN2 GIA 2GB | 2 cores | 2 GB | 40 GB SSD | 500 GB/mo | 1.2 Gbps | $89.99/mo · $899.99/yr | [ Order Tokyo 2GB](https://bwh81.net/aff.php?aff=77528&pid=108) |
| Tokyo CN2 GIA 4GB | 4 cores | 4 GB | 80 GB SSD | 1 TB/mo | 1.2 Gbps | $155.99/mo · $1559.99/yr | [ Order Tokyo 4GB](https://bwh81.net/aff.php?aff=77528&pid=109) |
| Tokyo CN2 GIA 8GB | 6 cores | 8 GB | 160 GB SSD | 2 TB/mo | 1.2 Gbps | $299.99/mo · $2999.99/yr | [ Order Tokyo 8GB](https://bwh81.net/aff.php?aff=77528&pid=110) |
| Tokyo CN2 GIA 16GB | 8 cores | 16 GB | 320 GB SSD | 4 TB/mo | 1.2 Gbps | $589.99/mo · $5899.99/yr | [ Order Tokyo 16GB](https://bwh81.net/aff.php?aff=77528&pid=111) |
| Tokyo CN2 GIA 32GB | 10 cores | 32 GB | 640 GB SSD | 6 TB/mo | 1.2 Gbps | $989.99/mo · $9989.99/yr | [ Order Tokyo 32GB](https://bwh81.net/aff.php?aff=77528&pid=123) |
| Tokyo CN2 GIA 64GB | 12 cores | 64 GB | 1 TB SSD | 8 TB/mo | 1.2 Gbps | $1889.99/mo · $18989.99/yr | [ Order Tokyo 64GB](https://bwh81.net/aff.php?aff=77528&pid=125) |

## Osaka CN2 GIA — Japan, Notably Cheaper Than Tokyo

Same hardware layout as Tokyo, 1.5 Gbps port, monthly pricing starts at $49.99 — roughly half Tokyo's $89.99 entry. Worth checking stock before assuming availability, since these plans rotate in and out.

| Plan | CPU | RAM | Storage | Transfer | Port | Billing | Order |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Osaka CN2 GIA 2GB | 2 cores | 2 GB | 40 GB SSD | 500 GB/mo | 1.5 Gbps | $49.99/mo · $499.99/yr | [ Order Osaka 2GB](https://bwh81.net/aff.php?aff=77528&pid=134) |
| Osaka CN2 GIA 4GB | 4 cores | 4 GB | 80 GB SSD | 1 TB/mo | 1.5 Gbps | $86.99/mo · $869.99/yr | [ Order Osaka 4GB](https://bwh81.net/aff.php?aff=77528&pid=135) |
| Osaka CN2 GIA 8GB | 6 cores | 8 GB | 160 GB SSD | 2 TB/mo | 1.5 Gbps | $165.99/mo · $1665.99/yr | [ Order Osaka 8GB](https://bwh81.net/aff.php?aff=77528&pid=136) |
| Osaka CN2 GIA 16GB | 8 cores | 16 GB | 320 GB SSD | 4 TB/mo | 1.5 Gbps | $329.99/mo · $3279.99/yr | [ Order Osaka 16GB](https://bwh81.net/aff.php?aff=77528&pid=137) |
| Osaka CN2 GIA 32GB | 10 cores | 32 GB | 640 GB SSD | 6 TB/mo | 1.5 Gbps | $549.99/mo · $5549.99/yr | [ Order Osaka 32GB](https://bwh81.net/aff.php?aff=77528&pid=138) |
| Osaka CN2 GIA 64GB | 12 cores | 64 GB | 1 TB SSD | 8 TB/mo | 1.5 Gbps | $1059.99/mo · $10559.99/yr | [ Order Osaka 64GB](https://bwh81.net/aff.php?aff=77528&pid=139) |

## Singapore CN2 GIA — Southeast Asia Coverage

Singapore mirrors Osaka's pricing and shares the same port speed progression (1.5 → 2.5 → 5 Gbps as you scale up). The right pick when your users are clustered in South China, Malaysia, Indonesia, or anywhere that benefits from SG peering over JP peering.

| Plan | CPU | RAM | Storage | Transfer | Port | Billing | Order |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Singapore CN2 GIA 2GB | 2 cores | 2 GB | 40 GB SSD | 500 GB/mo | 1.5 Gbps | $49.99/mo · $499.99/yr | [ Order SG 2GB](https://bwh81.net/aff.php?aff=77528&pid=173) |
| Singapore CN2 GIA 4GB | 4 cores | 4 GB | 80 GB SSD | 1 TB/mo | 1.5 Gbps | $86.99/mo · $869.99/yr | [ Order SG 4GB](https://bwh81.net/aff.php?aff=77528&pid=174) |
| Singapore CN2 GIA 8GB | 6 cores | 8 GB | 160 GB SSD | 2 TB/mo | 2.5 Gbps | $165.99/mo · $1665.99/yr | [ Order SG 8GB](https://bwh81.net/aff.php?aff=77528&pid=175) |
| Singapore CN2 GIA 16GB | 8 cores | 16 GB | 320 GB SSD | 4 TB/mo | 2.5 Gbps | $329.99/mo · $3199.99/yr | [ Order SG 16GB](https://bwh81.net/aff.php?aff=77528&pid=176) |
| Singapore CN2 GIA 32GB | 10 cores | 32 GB | 640 GB SSD | 6 TB/mo | 5 Gbps | $549.99/mo · $5549.99/yr | [ Order SG 32GB](https://bwh81.net/aff.php?aff=77528&pid=177) |
| Singapore CN2 GIA 64GB | 12 cores | 64 GB | 1 TB SSD | 8 TB/mo | 5 Gbps | $1059.99/mo · $10559.99/yr | [ Order SG 64GB](https://bwh81.net/aff.php?aff=77528&pid=178) |

## Dubai eCommerce — A Lower-Cost CN2 GIA-E Alternative

BandwagonHost also runs an eCommerce line out of Dubai (AEDXB_1) that shares the same migratable datacenter pool as the CN2 GIA-E plans — DC6 CN2 GIA-E, DC9 CN2 GIA, JPOS_1, EUNL_9, plus the standard US/EU locations. The entry plan drops to $19.99/month, which makes it the cheapest way onto the migratable CN2 GIA-E network if you don't need the VPS to physically sit in Los Angeles on day one. Transfer allowances are lower than the LA equivalents.

| Plan | CPU | RAM | Storage | Transfer | Port | Billing | Order |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Dubai 1GB | 2 cores | 1 GB | 20 GB SSD | 500 GB/mo | 1 Gbps | $19.99/mo · $169.99/yr | [ Order Dubai 1GB](https://bwh81.net/aff.php?aff=77528&pid=114) |
| Dubai 2GB | 3 cores | 2 GB | 40 GB SSD | 1 TB/mo | 1 Gbps | $32.99/mo · $299.99/yr | [ Order Dubai 2GB](https://bwh81.net/aff.php?aff=77528&pid=115) |
| Dubai 4GB | 4 cores | 4 GB | 80 GB SSD | 2 TB/mo | 1 Gbps | $56.99/mo · $549.99/yr | [ Order Dubai 4GB](https://bwh81.net/aff.php?aff=77528&pid=116) |
| Dubai 8GB | 6 cores | 8 GB | 160 GB SSD | 3 TB/mo | 1 Gbps | $86.99/mo · $879.99/yr | [ Order Dubai 8GB](https://bwh81.net/aff.php?aff=77528&pid=117) |
| Dubai 16GB | 8 cores | 16 GB | 320 GB SSD | 4 TB/mo | 1 Gbps | $159.99/mo · $1599.99/yr | [ Order Dubai 16GB](https://bwh81.net/aff.php?aff=77528&pid=118) |
| Dubai 32GB | 10 cores | 32 GB | 640 GB SSD | 5 TB/mo | 1 Gbps | $289.99/mo · $2759.99/yr | [ Order Dubai 32GB](https://bwh81.net/aff.php?aff=77528&pid=119) |
| Dubai 64GB | 12 cores | 64 GB | 1 TB SSD | 6 TB/mo | 1 Gbps | $549.99/mo · $5399.99/yr | [ Order Dubai 64GB](https://bwh81.net/aff.php?aff=77528&pid=120) |

## SLA Plans — When Downtime Costs More Than the VPS

A separate product line adds a 99.99% uptime SLA and dedicated IP on top of the CN2 GIA-E network. Worth it when the box is in front of paying customers and a 30-minute outage costs more than a year of VPS billing.

| Plan | CPU | RAM | Storage | Transfer | Port | Billing | Order |
| --- | --- | --- | --- | --- | --- | --- | --- |
| SLA 1GB | 2 cores | 1 GB | 20 GB SSD | 1 TB/mo | 2.5 Gbps | $65.89/qtr · $239.99/yr | [ Order SLA 1GB](https://bwh81.net/aff.php?aff=77528&pid=164) |
| SLA 2GB | 3 cores | 2 GB | 40 GB SSD | 2 TB/mo | 2.5 Gbps | $116.99/qtr · $399.99/yr | [ Order SLA 2GB](https://bwh81.net/aff.php?aff=77528&pid=165) |

## Limited Edition Plans — The $49.99/Year Sweet Spot

BandwagonHost periodically drops limited-edition plans at promotional annual prices. These show up in restock alerts and sell out fast:

- **DC6 CN2 GIA-E Limited Edition** — 1 core / 512 MB / 10 GB SSD / 500 GB/mo / 1 Gbps — around $49.99/year. The cheapest legitimate way onto the CN2 GIA-E network.
- **Los Angeles 10G KVM PROMO V5 CN2 GIA** — 1 core / 512 MB / 10 GB SSD / 500 GB/mo / 1.5 Gbps — around $49.90/year. DC6-eligible.
- **BiggerBox Pro (DC1)** — 1 core / 1 GB / 20 GB SSD / 1 TB/mo / 2.5 Gbps — around $39/year. Tri-network CN2 GIA + CMI + Unicom Premium.

A few honest caveats BandwagonHost itself flags: limited plans can vanish at checkout without notice, renewal pricing may not match the promo price, and some have migration restrictions. Treat them as opportunities, not as your only plan. Always confirm stock on the official order page before relying on one. You can check current availability 👉 [Browse the full CN2 GIA catalog](https://bit.ly/BandWaGon).

## Promo Codes — What's Currently Working

The promo code situation shifts over time. As of the most recent verified updates:

- **NODESEEK2026** — recurring 6.77% discount on standard plans. Currently the most-cited working code.
- **Bigger drops on Double 11 and Black Friday** — historically the deepest discounts of the year, often bringing limited-edition plans back into stock at the same time.

Older codes (BWH3HYATVTRW, BWHCCNCXVV, BWHNY2022 and similar) have largely expired. If a code doesn't apply at checkout, it's not you — it's the code. Promo eligibility also varies by plan; the system will tell you at the cart stage whether a code applies. Don't assume a code will work on every product line.

## Purchase Walkthrough — From Order Page to KiwiVM

The flow is short enough that you can be inside your VPS within ten minutes of clicking "Order Now."

1. **Pick a plan** from the comparison tables above. The order link drops you onto the configuration page for that specific product.
2. **Choose billing cycle** — monthly, quarterly, semi-annual, or annual. Annual pricing is consistently the cheapest per month across every family.
3. **Pick a datacenter** from the locations available for that plan. CN2 GIA-E plans give you the most choice; Hong Kong/Tokyo/Osaka/Singapore are locked to their respective cities (with free migration between Asia CN2 GIA locations).
4. **Apply promo code** in the cart before checkout. NODESEEK2026 is the current reliable one.
5. **Register or log in** — email, password, real-name-style contact info (use Pinyin if you don't have a Western name; don't pay through a VPN, BandwagonHost flags that).
6. **Pay** via Alipay, UnionPay, PayPal, or credit card. Alipay is the path most China-based users take.
7. **Check email** for service activation details, then log into the in-house KiwiVM panel to reload the OS, set rDNS, migrate datacenters, or pull usage stats.

On OS selection: AlmaLinux, RockyLinux, CentOS, Debian, Ubuntu, CentOS Stream, and Fedora are all pre-loaded templates. Custom ISOs can be added on request.

## Choosing the Right Plan — A Practical Decision Tree

The comparison tables above give you the raw data. Here's how to actually use it.

**Budget-first, just need CN2 GIA routing for a personal proxy, light site, or dev box:** Grab the CN2 GIA-E 1GB at $49.99/quarter (or the $49.99/year limited edition if you catch a restock). It's the cheapest fully-featured CN2 GIA-E plan in the catalog and migrates across 11+ datacenters for free. 👉 [Order CN2 GIA-E 1GB](https://bwh81.net/aff.php?aff=77528&pid=87).

**Lowest possible latency from Mainland China:** Hong Kong CN2 GIA 2GB at $89.99/month. 30–60 ms to most Chinese metros, hard to beat for anything interactive. 👉 [Order HK 2GB](https://bwh81.net/aff.php?aff=77528&pid=95).

**Hong Kong out of stock, or you want a touch more bandwidth:** Tokyo CN2 GIA 2GB at the same $89.99/month price, 1.2 Gbps port instead of 1 Gbps, ~40–80 ms latency. 👉 [Order Tokyo 2GB](https://bwh81.net/aff.php?aff=77528&pid=108).

**Price-sensitive but still want Asia routing:** Osaka or Singapore CN2 GIA 2GB at $49.99/month — half the entry price of Tokyo/HK, same CPU/RAM/storage footprint, slightly larger port. 👉 [Order Osaka 2GB](https://bwh81.net/aff.php?aff=77528&pid=134) or 👉 [Order SG 2GB](https://bwh81.net/aff.php?aff=77528&pid=173).

**Heavier traffic — video, large file distribution, build pipelines:** Move up the CN2 GIA-E stack. The 8GB at $86.99/month jumps you to a 5 Gbps port and 5 TB of transfer, which is roughly the point where bandwidth stops being a constraint for most use cases. 👉 [Order CN2 GIA-E 8GB](https://bwh81.net/aff.php?aff=77528&pid=90).

**Mission-critical workloads in front of paying customers:** The SLA plans add a 99.99% uptime SLA and dedicated IP for a modest premium. Worth it when downtime costs more than the VPS itself. 👉 [Order SLA 1GB](https://bwh81.net/aff.php?aff=77528&pid=164).

## What Real Users Say

A few consistent themes from long-term user reviews and third-party testing:

- **Stability under load** — Los Angeles DC6 CN2 GIA-E holds 200–400 Mbps sustained from China on downloads, even during peak hours, significantly better than 163-network alternatives.
- **Latency reality check** — Hong Kong's 30–60 ms is genuinely the dream-tier experience for China users; Los Angeles sits around 150–180 ms but compensates with bandwidth and tri-network routing.
- **The KiwiVM panel** — frequently called out as a strength: snapshots, free datacenter migration, one-click OS reloads, and an API all included. The self-managed model keeps prices down, but the panel makes self-management genuinely easy.
- **Support expectations** — it's self-managed, so don't expect hand-holding on application-layer issues. Network and hardware issues are monitored 24/7 and acted on proactively.
- **Price creep over time** — several reviewers note that the cheapest CN2 GIA plans have crept up over the years; the $39.99/year tier is gone, and the $49.99/year tier is now limited-edition only. The general consensus is that current pricing is still competitive for what CN2 GIA actually costs to provide.

## Final Take

BandwagonHost's CN2 GIA lineup isn't the cheapest VPS catalog on the internet, and it isn't trying to be. What it offers is reliable, low-packet-loss routing into Mainland China across five distinct geographic options, with a flexible in-house control panel and a pricing structure that scales cleanly from a $49.99/quarter personal box up to a $1889.99/month enterprise rig.

For most readers landing on this page, the answer is straightforward: start with CN2 GIA-E out of Los Angeles, pick the RAM tier that matches your workload, pay annually to lock in the per-month discount, and apply NODESEEK2026 at checkout. If latency turns out to be the bottleneck, the free datacenter migration feature lets you hop over to Hong Kong or Tokyo later without losing your data.

Ready to pick a plan? 👉 [Browse the full CN2 GIA catalog and lock in current pricing](https://bit.ly/BandWaGon).
