# RainYun review: node-by-node prices and measured performance, so you pick the right plan without overpaying

Most "RainYun review" searches come from the same place: someone saw a Hong Kong or US VPS advertised at ¥20-something a month, and wants to know whether the number is real, whether the network is usable, and whether a Chinese provider will let them pay from outside China.

Short version: the prices are real, but the number on the banner is a stacked discount, not list price, and what you get depends enormously on which zone you pick. RainYun runs nodes in mainland China, Hong Kong, Japan, the US and Germany, and the cheap headline plans sit in completely different network situations. Below is what each tier actually costs, what third-party tests measured, and where the catches are.

## What RainYun actually is

RainYun (雨云) has been operating since 2018 and builds its own billing and product systems rather than reselling someone else's panel — unusual at this price point. It holds ISP, IDC and CDN licences issued by China's Ministry of Industry and Information Technology, which matters if you care about your host being a licensed operator rather than a one-person reseller.

The product line is broader than the VPS ads suggest: KVM cloud servers, bare-metal dedicated servers, second-generation virtual hosting in two panel flavours (BT Panel and EasyPanel), a game-cloud line built on high-clock consumer CPUs, object storage, CDN, backup storage, Kubernetes-based "cloud apps", and GPU cloud desktops.

For a quick look at the lineup and current sign-up bonus, 👉 [check RainYun's plans and first-month discount](https://www.rainyun.com/MzA2MTc2_).

## Read the discount stack before you read the price

This is the single most important thing to understand about RainYun's pricing, and it's where most review posts quietly mislead you.

| Payment term | Discount | You pay |
| --- | --- | --- |
| 1 month | none | list price |
| 3 months | 10% off | 90% of list |
| 6 months | 20% off | 80% of list |
| 12 months | 30% off | 70% of list |

On top of that, new accounts get a **50%-off first-month coupon** (usually by registering with a promo code or binding WeChat), and an **80%-off purchase coupon** is available from the points mall. Those two stack: 0.8 × 0.7 = **56% of list price** on an annual purchase, which is exactly where numbers like "¥21.28/month" come from. The plan's list price is ¥38.

So when a review headline says "2 cores, 2GB, 50Mbps for ¥21/month", that's a new customer, annual, coupon-stacked figure. Month-to-month at list price it's ¥38. Renewal doesn't repeat the first-month coupon. Plan your budget against list price and treat the discount as a bonus.

The 7折 annual rate is applied platform-wide, though a community purchasing guide notes that the Hubei Shiyan zone is excluded from the annual discount — treat that as user-reported rather than a guarantee.

## Overseas cloud servers: the four zones that matter

RainYun splits overseas cloud servers into **metered bandwidth** (fast port, capped monthly traffic) and **unmetered** (slow port, no traffic cap). Same CPU and RAM, same price, different network shape. Pick the wrong one and you'll be throttled or crawling.

### Hong Kong, CN2 GIA triple-network direct

This is the line reviewers describe as CN2 GIA-optimised with direct routes for all three Chinese carriers. List prices:

| Plan | vCPU | RAM | Disk | Bandwidth | Traffic | Price/mo |
| --- | --- | --- | --- | --- | --- | --- |
| Plan 1 | 1 | 1GB | 30GB | 10Mbps | 20GB | ¥25 |
| Plan 2 | 2 | 2GB | 30GB | 20Mbps | 50GB | ¥33 |
| Plan 3 | 2 | 4GB | 30GB | 30Mbps | 50GB | ¥48 |
| Plan 4 | 4 | 4GB | 30GB | 40Mbps | 50GB | ¥64 |

The unmetered versions carry identical prices with ports of 3, 5, 8 and 10Mbps respectively. That's the trade in plain terms: 40Mbps that dies at 50GB, or 10Mbps that runs all month.

👉 [See current Hong Kong triple-network pricing](https://www.rainyun.com/MzA2MTc2_)

### United States, Los Angeles (AMD EPYC 7702, unmetered)

| Plan | vCPU | RAM | Disk | Bandwidth (up/down) | Price/mo |
| --- | --- | --- | --- | --- | --- |
| KVM Entry | 1 | 1GB | 30–2000GB | 20M / 30M | ¥25 |
| KVM Standard | 2 | 2GB | 30–2000GB | 30M / 50M | ¥34 |
| KVM Mid | 2 | 4GB | 30–2000GB | 40M / 60M | ¥44 |
| KVM Advanced | 4 | 4GB | 30–2000GB | 60M / 80M | ¥60 |
| KVM High | 4 | 8GB | 30–2000GB | 80M / 100M | ¥113 |
| KVM Flagship | 8 | 16GB | 30–2000GB | 100M / 150M | ¥197 |

A published US test on the Los Angeles dual-line node returned US-region unlocks across the board — Netflix, Disney+, Google services and Claude all resolved as native US rather than proxied. If your reason for buying a US IP is streaming or US-only APIs, that's the relevant data point.

### Hong Kong, Xeon Gold traffic-stacking line

| Plan | vCPU | RAM | Disk | Bandwidth (up/down) | Price/mo |
| --- | --- | --- | --- | --- | --- |
| KVM Entry | 1 | 1GB | 30–2000GB | 10M / 10M | ¥28 |
| KVM Standard | 2 | 2GB | 30–2000GB | 20M / 20M | ¥35 |
| KVM Mid | 2 | 4GB | 30–2000GB | 20M / 20M | ¥48 |
| KVM High | 4 | 4GB | 30–2000GB | 30M / 30M | ¥68 |
| KVM Top | 4 | 8GB | 30–2000GB | 30M / 30M | ¥108 |
| KVM Flagship | 8 | 16GB | 30–2000GB | 50M / 50M | ¥188 |

"Traffic-stacking" means unused monthly traffic rolls into the next month instead of expiring. Run a low-traffic site and the allowance accumulates.

## The budget nodes: where the ¥16–¥35 headlines live

These are the zones that generate the cheap screenshots. Prices below are the stacked annual-and-coupon figures as published in the review write-ups, so compare them mentally against the list price.

| Node | vCPU | RAM | Bandwidth | Traffic | Stacked price/mo |
| --- | --- | --- | --- | --- | --- |
| Hong Kong Zone 2 (CMI) | 2 | 2GB | 50Mbps | 100GB | ¥21.28 |
| Hong Kong Zone 2 | 4 | 8GB | 80Mbps | 200GB+ | ¥74.48 |
| Hong Kong Zone 5 (big bandwidth) | 2 | 2GB | 500Mbps | metered | ¥19.60 |
| Hong Kong Zone 5 | 2 | 2GB | 1000Mbps | 1024GB | ¥35.00 |
| Hong Kong Zone 5 | 4 | 8GB | 1000Mbps | metered | ¥60.48 |
| Japan Tokyo Zone 2 (SoftBank) | 1 | 1GB | 50Mbps | metered | ¥16.80 |
| Japan Tokyo Zone 2 (SoftBank) | 2 | 4GB | 100Mbps | 500GB | ¥26.32 |
| Germany Frankfurt Zone 1 | 2 | 4GB | 100Mbps | 200GB | ¥35.28 |
| Germany Frankfurt Zone 1 | 4 | 8GB | 200Mbps | metered | ¥85.68 |

Two things worth knowing before you chase the cheapest row. Hong Kong Zone 2 had no stock at the time the reviews were written and the authors pointed readers toward Zone 3 instead — popular zones sell out. And the hardware across these budget tiers is AMD EPYC 7K62 or 7452 with 30GB SSD, so you're not getting a slow chip, you're getting a small one.

👉 [Check which budget nodes are in stock right now](https://www.rainyun.com/MzA2MTc2_)

## Mainland China nodes: high protection is the actual selling point

China-based deployments are a different product. The Wenzhou (Zhejiang) node pairs a 100Mbps port and 100GB disk with **100Gbps DDoS protection included**, and latency tests across the three major carriers averaged roughly 41ms nationally — around 30ms on Telecom, 35ms on Mobile, 44ms on Unicom. Packet loss was measured at 0%.

| Plan | vCPU | RAM | Disk | Bandwidth | Traffic | Price/mo |
| --- | --- | --- | --- | --- | --- | --- |
| Plan 1 | 2 | 2GB | 100GB | 100Mbps | 300GB | ¥38 |
| Plan 2 | 2 | 4GB | 100GB | 100Mbps | 300GB | ¥48 |
| Plan 3 | 4 | 4GB | 100GB | 100Mbps | 500GB | ¥75 |
| Plan 4 | 4 | 8GB | 100GB | 100Mbps | 500GB | ¥88 |

Note the discrepancy that shows up in RainYun's own community: a forum test of the *unmetered* Wenzhou 4-core/8GB quotes ¥128/month at list and ¥823.20–¥1,243.20 per year on the annual discount for the 2-core and 4-core models respectively. Metered and unmetered are priced separately, so the table above is the metered lineup, not the whole node.

Other mainland zones include Suqian (Jiangsu), Shiyan and Xiangyang (Hubei), Shenzhen, Chongqing and Ningbo. Hubei and Suqian offer up to several hundred gigabits of protection on dedicated IPs. Fair warning: mainland services require Chinese real-name verification and, for web hosting, ICP filing. Overseas zones don't.

If your audience is in China, mainland beats Hong Kong on both latency and cost per gigabit. If your audience isn't, it doesn't.

## Game cloud: high-clock CPUs at prices mainstream clouds can't match

The game-cloud line uses consumer-grade high-frequency silicon rather than server chips — the logic being that Minecraft and similar servers care far more about single-thread speed than core count. Fixed-billing list prices:

| CPU | vCPU | RAM | Bandwidth | System + data disk | Price/mo |
| --- | --- | --- | --- | --- | --- |
| E5-2666v3 | 2 | 4GB | 10Mbps | 30GB + 20GB | ¥65 |
| Gold 6146 | 2 | 4GB | 10Mbps | 30GB + 20GB | ¥80 |
| Ryzen 5900X | 1 | 2GB | 5Mbps | 30GB + 20GB | ¥125 |
| Ryzen 7950X | 1 | 2GB | 5Mbps | 30GB + 20GB | ¥139 |
| i9-13900KF | 1 | 2GB | 5Mbps | 30GB + 20GB | ¥145 |
| i9-14900KF | 1 | 2GB | 5Mbps | 30GB + 20GB | ¥145 |

These are NAT instances sharing a public IP, with up to 15 port mappings — fine for a private server, awkward for anything that needs port 25565 on a clean address. Dedicated IPs cost extra and vary a lot by node: ¥50/month in Hubei Shiyan, ¥60/month for a 100G-protected Wenzhou IP, and ¥150/month in Suqian because the dedicated IP carries its own 150Gbps of protection.

There's also a **dynamic billing** mode, where the monthly cost moves with actual CPU usage. For a server that's busy two evenings a week and idle otherwise, that's usually the better deal.

👉 [Compare game cloud CPUs and billing modes](https://www.rainyun.com/MzA2MTc2_)

## Virtual hosting, if you just want a website

Virtual hosting is the cheapest way in. Second-generation plans come with either BT Panel (full panel, root-ish control, arbitrary software versions, SSH/SFTP) or EasyPanel (simpler, five-domain limit, one database). The US EasyPanel node includes a **¥0 plan** — 1 core, 512MB RAM, 5GB disk, 2Mbps up / 5Mbps down — which is the rare genuinely free hosting offer that isn't a 14-day trial.

Representative published prices:

| Node | Panel | Tier | Storage | Price/mo |
| --- | --- | --- | --- | --- |
| Zaozhuang | EasyPanel 2nd gen (ICP filing required) | Entry | 0.5GB | ¥7 (promo ¥6) |
| Zaozhuang | EasyPanel 2nd gen | Standard | 1GB | ¥9 |
| Zaozhuang | EasyPanel 2nd gen | High | 3GB | ¥14 |
| Zaozhuang | EasyPanel 2nd gen | Top | 8GB | ¥24 |
| Hong Kong | EasyPanel 2nd gen (no filing) | Standard | 1GB | ¥10 |
| Hong Kong | EasyPanel 2nd gen | High | 3GB | ¥15 |
| Hong Kong | EasyPanel 2nd gen | Top | 8GB | ¥25 |
| Zaozhuang | BT Panel 2nd gen (LXD) | High | 20GB | ¥33 |
| Zaozhuang | BT Panel 2nd gen (LXD) | Top | 45GB | ¥49 |
| Hong Kong | BT Panel 2nd gen (LXD) | High | 20GB | ¥35 |
| US | BT Panel 2nd gen (LXD) | Standard | 10GB | ¥20 |
| US | BT Panel 2nd gen (LXD) | High | 20GB | ¥28 |
| US | BT Panel 2nd gen (LXD) | Top | 45GB | ¥46 |
| US | BT Panel 2nd gen | Free | 5GB | ¥0 |

Nodes and tiers shift with stock, so the configurator will show the current regional lineup. Hong Kong and US nodes skip China's ICP filing; Zaozhuang does not.

A published benchmark of the Hong Kong BT Panel High plan (2 cores, 2GB, 20GB, 8Mbps up/down, Xeon E5-2690 v4) recorded roughly 630 single-core and 886 multi-core, with round-trip latency of 58–103ms to Chinese cities and clean unlocks for Netflix, Disney+ and TVBAnywhere+. It also can't use IPv6.

👉 [See current virtual hosting plans and the free tier](https://www.rainyun.com/MzA2MTc2_)

## What the benchmarks and the small print actually tell you

Strip out the marketing and a consistent picture emerges from independent tests:

**Network, not CPU, is what you're buying.** A Hong Kong Zone 2 test measured ~56ms average latency with a 32ms best case via Shanghai Telecom, direct routes outbound on all three carriers, and CMI return routing. Bandwidth tests hit roughly 50.5Mbps down and 50.0Mbps up on a 50Mbps plan, with CPU scores around 1,598 single-core and 3,123 multi-core on LemonBench, 1,126/2,052 on Geekbench 6.

**The traffic policy is more forgiving than most.** Run out and you're throttled to 5Mbps rather than suspended, and unused traffic carries over. Top-up packages vary by region — 200GB for ¥50 or 1TB for ¥200 in Hong Kong, 500GB for ¥50 or 1TB for ¥80 in Japan.

**Mail ports are restricted.** Multiple tests flag this. Don't buy RainYun for outbound bulk mail; you'll be blocked and it's your own fault for not reading the notes.

**DDoS protection is node-specific, not platform-wide.** The Wenzhou and Suqian nodes advertise 100–200Gbps. Hong Kong Zone 2 explicitly has *no* protection. If you're targeted, the cheap zone is the wrong zone.

**Extra costs add up quietly.** Disk expansion runs ¥0.4/GB/month on SSD cloud disks and ¥0.1/GB/month on efficient disks. Extra IPv4 addresses are ¥5 each; high-protection IPs are ¥30–¥60/month. Backup storage is free for the first 5GB once you bind WeChat, then ¥0.003/GB/day.

**Payment is Alipay and WeChat Pay** — no international cards. For buyers outside China, that's the practical blocker, not the price.

## The refund policy has a trap in it

RainYun advertises a **7-day no-reason refund, up to three times per account**, plus a ¥1 one-day trial on cloud server and game cloud products (once per product). Both are real.

But there's a condition that shows up repeatedly in the community forum. In a thread from a customer whose server was dropping connections, staff refused two consecutive refund requests with a single line: the account had already claimed **consumption points** (消费积分), which disqualifies the product from no-reason withdrawal. Other users in the same thread noted that the points-claim dialog does warn you about this before you confirm.

The lesson is straightforward: if there's any chance you'll want your money back, **don't claim the points on that order**. Test first with the ¥1 trial, confirm the node's network behaves for your use case, then commit and collect the points.

## The free tier is real, and it isn't a trial

RainYun's points system is unusual and worth understanding, because it changes the economics at the low end. Points accrue from daily sign-in (500/day) and one-off account tasks (binding email, phone, WeChat, joining the QQ group — around 8,700 points for the whole set). The conversion rate is 2,000 points = ¥1, and points can be withdrawn from 60,000 points (¥30) upward.

Those points buy things in the points mall, including **free game cloud instances** and free virtual hosting, restocked around 20:00 daily and gone quickly. Free game instances run for a seven-day term and are renewed with points — the accounts that keep a Minecraft server alive for free are the ones that sign in every day. It's a real mechanism, not a marketing hook, but it's also a small daily chore, and stock is genuinely limited.

Free resources come with the obvious caveats: shared panel environments, fewer resources, and no priority when something breaks.

## Who should buy, who shouldn't

**A good fit if** you're serving users in mainland China or need cheap Hong Kong/Japan connectivity for a China-facing project; you want high-clock hardware for a game server at a price the big clouds won't quote; you want full control of a China-licensed operator with self-built billing; or you want a site host with a free tier to test on.

**A poor fit if** you need international card payments and English-language support as a baseline; you need European or North American latency for a Western audience (Frankfurt test numbers show roughly 163ms average to China, and the LA node exists mainly for US unlocks); you're sending mail; you need a clean native IP for account registration on platforms that treat datacenter ranges harshly; or you want to be able to walk away after using the points without checking the refund rules first.

## Practical first steps

1. Read the zone you want before you buy. Hong Kong Zone 2 and Zone 5 are completely different products at similar prices.
2. Decide metered or unmetered first, then pick cores. Wrong choice here costs more than wrong CPU.
3. Use the ¥1 one-day trial on the exact plan you're considering.
4. If you're staying, buy annually — 30% off is the largest single discount and it's permanent for each term.
5. Skip the points claim until you're sure you're keeping the server.

For the full current lineup, node availability and the first-month discount, 👉 [start here on RainYun](https://www.rainyun.com/MzA2MTc2_).

## FAQ

**Is RainYun legit or a reseller?**
It's been operating since 2018, develops its own financial and product systems, and holds MIIT-issued ISP, IDC and CDN licences — that's a licensed operator, not a rebranded reseller.

**Can I pay with a credit card?**
Not directly. Alipay and WeChat Pay are the payment methods, so you need one of those accounts.

**Is the network good outside China?**
Mainland latency is where it performs. Frankfurt tests show around 163ms average to China; Los Angeles prioritises US-region services. If your users are European or North American, test the specific node before committing.

**What happens when I use up my traffic?**
You're throttled to 5Mbps, not cut off, and leftovers roll over. Higher-speed traffic can be bought back in packages.

**Do I need ICP filing?**
For mainland China nodes used for web hosting, yes, plus Chinese real-name verification. Hong Kong, Japan, Germany and US nodes don't require filing.

**Is the free plan actually free?**
The US EasyPanel virtual hosting tier is ¥0/month, and free game cloud instances are exchangeable for points with renewal at no cash cost — but stock is limited and renewal depends on you signing in.
