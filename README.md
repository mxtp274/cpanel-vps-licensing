# vps hosting with cpanel and whm: what the cPanel license really costs, how bundled and add-on hosts compare, and the plans that make sense for resellers and multi-site owners

Most people searching for VPS hosting with cPanel and WHM already know what they want: a server they control at the root level, WHM to create and manage hosting accounts, and cPanel for the day-to-day work on each site. What trip people up aren't the VPS specs — it's the cPanel/WHM license. Some providers bundle the license into the plan price and charge you a clearly higher monthly rate for it. Others sell you a dirt-cheap VPS and treat the license as a paid add-on you configure at checkout. Both models work, but they produce very different bills depending on how many accounts you actually run.

That second model is where RackNerd lives. RackNerd sells budget KVM VPS plans — famously cheap annual specials — and lets you attach a cPanel/WHM license to the server during the order process, priced by the account tier you pick. If you're comfortable being your own sysadmin, that combo is usually the cheapest way to run a proper cPanel stack. If you'd rather never think about licensing, the bundled hosts make more sense. This article walks through the real numbers, the full plan lineup, and where each approach wins.

> **Quick picks**
> - Running a handful of sites (yours or a few clients'): RackNerd's **2.5GB special at $24.99/year** plus a cPanel Admin license add-on lands around **$13–17/month all-in** with room for up to 30 accounts.
> - Just one site: the cheapest special plus a Solo license keeps the whole stack under roughly $8/month.
> - Reselling with many accounts, or you want the provider handling server issues: a license-included host will serve you better — the comparison table below has the details.
> - 👉 [See RackNerd's current KVM VPS specials and add a cPanel/WHM license at checkout](https://bit.ly/my-rn)

## What you're actually buying with cPanel VPS hosting

You're buying two control panels that ship together under one license. WHM is the server-level panel: you use it to create hosting accounts, define packages with resource limits, manage DNS zones and nameservers, and configure server-wide settings. cPanel is what each account holder gets — files, email, databases, SSL, domains — with no visibility into anyone else's account. On shared hosting you only ever see the cPanel side; a VPS with root access is the first tier where you get the full WHM view too, which is exactly why this setup is the starting point for hosting clients' sites.

Practical details worth knowing before you buy: cPanel is normally reached on port 2082 (or 2083 over SSL), WHM on 2086/2087. The panels support automation through command-line tools and an API, so once accounts multiply you can script provisioning instead of clicking through everything. Email, AutoSSL certificates, and per-account backups all come from the panel stack itself rather than from the hosting provider, which is why the license model matters more than most marketing pages admit.

## RackNerd's plans: cheap KVM VPS, with cPanel/WHM added at checkout

RackNerd doesn't sell a separate "cPanel VPS" product. You pick one of their KVM VPS plans, choose an operating system image, and add the cPanel/WHM license as a configurable add-on in the same order flow. The license is tiered by account count the way cPanel licenses work everywhere: Solo covers a single account, Admin covers up to 30, Pro up to 100, and Premium beyond that. The VPS itself is the cheap part — their annual specials are among the lowest prices you'll find on KVM virtualization with SSD storage.

Here are the core tiers that make sense as cPanel hosts:

| Plan (promo) | vCPU / RAM | SSD storage | Monthly transfer | Price | Order |
| --- | --- | --- | --- | --- | --- |
| 1GB Special | 1 vCPU / 1GB | 20GB SSD | 1TB | $10.99/yr | [ Order this plan](https://bit.ly/my-rn) |
| 2.5GB Special | 2 vCPU / 2.5GB | 40GB SSD | 4TB | $24.99/yr | [ Order this plan](https://bit.ly/my-rn) |
| 4GB Special | 3 vCPU / 4GB | 60GB SSD | 5TB | $39.99/yr | [ Order this plan](https://bit.ly/my-rn) |
| 6GB Special | 4 vCPU / 6GB | 90GB SSD | 6TB | $59.99/yr | [ Order this plan](https://bit.ly/my-rn) |
| 10GB Special | 5 vCPU / 10GB | 150GB SSD | 8TB | $89.99/yr | [ Order this plan](https://bit.ly/my-rn) |

A few things the table can't show. These specials bill annually; monthly terms exist on their standard KVM page at higher rates. RackNerd runs data centers in Los Angeles, San Jose, Seattle, Dallas, Chicago, New York, Atlanta, and Amsterdam, so pick the location closest to your visitors. Every plan includes root access and a dedicated IPv4, and their promo pricing carries over to renewals — the rate you sign up at is the rate you keep, which is unusual at this price point and matters a lot for multi-year budgeting.

One flag: RackNerd is unmanaged. Ticket support handles the server being up and reachable; it doesn't tune your mail server or debug your WordPress install. That's the trade you make for the pricing.

## The license math that decides whether RackNerd is actually cheaper

The VPS is a fraction of the bill. The license dominates it.

cPanel reseller pricing varies, but the pattern is stable: a Solo license (one account) typically runs under $6/month, an Admin license (30 accounts) lands somewhere around $10–15/month, and Pro/Premium tiers climb from there. So on RackNerd, your true monthly cost looks like this:

- **2.5GB special ($24.99/yr ≈ $2.08/mo) + Admin license ≈ $12–17/month all-in** for 2 vCPU, 2.5GB RAM, 40GB SSD, and capacity for 30 accounts.
- Solo route: same VPS or the 1GB plan plus a Solo license puts a single-site stack at roughly $7–8/month.
- 4GB special ($3.33/mo) + Admin license ≈ $13–18/month — comfortable for 10+ modest WordPress sites.

Now compare that against license-included hosts. HostOy's VPS-2 is $20/month (billed $240/year) with 2 vCPU, 4GB RAM, 60GB NVMe, and the cPanel/WHM license baked in. InterServer's 4-slice plan is $12/month for 8GB RAM and 160GB SSD, with the cPanel option configured during ordering as a separate line item. PingRack bundles the license into plans starting at ₹1,199/month (roughly $14) with a 25-account cap on the starter tier, and Ucartz includes the license at $25.46/month on its current 33%-off promo.

Reading those numbers honestly: for one to five accounts over a two-to-three-year horizon, RackNerd plus an add-on license wins on total cost, and the locked renewal price keeps it winning. Past roughly ten accounts — or the moment you want CloudLinux account isolation, managed support, or somebody else to own the licensing relationship — the bundled hosts stop looking expensive and start looking like the sensible option. InterServer deserves a specific mention here: its slice model (1 to 32 slices) scales in small steps, and managed support kicks in from 8 slices at $24/month, which is a genuinely different product than an unmanaged $25/year VPS.

- 👉 [Check RackNerd's current promo pricing before the next sale cycle changes the numbers](https://bit.ly/my-rn)

## Ordering a cPanel VPS from RackNerd: four steps and two easy mistakes

The checkout flow is short, but two wrong turns are common enough to warn about.

1. **Choose your plan and term.** The specials bill annually. Pick the RAM tier based on your account count, not the sticker price.
2. **Select the OS image: AlmaLinux 9.** cPanel runs on AlmaLinux, Rocky Linux, CloudLinux, and Ubuntu LTS. AlmaLinux 9 is the safe default for new deployments — it's also what PingRack recommends in their own cPanel FAQ, for what it's worth.
3. **Add the cPanel/WHM license add-on** and pick the tier matching your expected account count, with a little headroom. Starting at Admin when you'll host more than a couple of sites saves you an upgrade later, though license upgrades are straightforward if you outgrow Solo.
4. **After provisioning, log into WHM** at your server IP on port 2087, set your nameservers, create your first accounts, and let AutoSSL issue certificates.

The two mistakes, then. First: buying the 1GB plan for cPanel. It will install, and it might even survive a week, but once you enable mail scanning, run a database or three, and put actual traffic on a site, 1GB swaps itself into the ground. Treat 2.5GB as the floor and 4GB as the comfortable zone. Second: the license binds to your server's IP at deployment. Don't build your hosting on a plan to shuffle IPs later — changing them means re-confirming the license, and it's the kind of friction you don't need on day one.

- 👉 [Start the RackNerd order flow and pick your plan, OS, and license tier in one pass](https://bit.ly/my-rn)

## How RackNerd stacks up against license-included cPanel hosts

Here's the field, information only. No host here is "best" across the board — the right pick depends on which row matters to you.

| Host | Cheapest cPanel-ready plan | License | Storage | Worth knowing |
| --- | --- | --- | --- | --- |
| RackNerd | $10.99/yr (1GB special; add license for cPanel) | Paid add-on, tiered by account count | SSD | Promo rate locked at renewal; unmanaged |
| InterServer | $12/mo (4 slices: 8GB RAM, 160GB SSD) | Added in order flow, separate cost | SSD | Managed support included from 8 slices; scales 1–32 slices |
| HostOy | $12/mo, billed annually (1 vCPU, 2GB, 30GB) | Included | NVMe | 99.99% uptime SLA claim; 30-day money-back; managed positioning |
| PingRack | ₹1,199/mo (2 vCPU, 4GB, 80GB) | Included | NVMe | 25-account cap on starter; CloudLinux + CageFS from Business tier; free cPanel-to-cPanel migration |
| Ucartz | $25.46/mo (1 vCPU, 2GB, 50GB) | Included | HDD | 33%-off promo pricing shown; free migration; 99.9% uptime SLA |
| LightNode | $7.71/mo (1 vCPU, 2GB, 50GB NVMe) | cPanel pre-installed — confirm license billing at checkout | NVMe | Hourly billing model; 40+ global locations |

Where each one genuinely fits: InterServer if you expect steady growth and want managed support without jumping to a dedicated server. HostOy if the 30-day money-back window and managed cPanel positioning lower your risk tolerance. PingRack or Ucartz if reselling with many isolated accounts is the goal — CloudLinux's per-account resource limits come standard on PingRack's Business tier and up, and Ucartz includes migration assistance, though note its storage is HDD rather than SSD. LightNode is the pick when geographic coverage or short, hourly commitments matter more than absolute price.

Ucartz is also the honest counterweight to RackNerd's low sticker price: $25.46/month all-in with no license decisions is a real offer, even if the raw VPS underneath costs more than RackNerd's.

## When RackNerd is the wrong choice for cPanel hosting

Being straight about the downsides, because they're real:

- **You don't want to be the sysadmin.** On an unmanaged VPS, OS updates, security hardening, firewall rules, and email deliverability are your job. If a bounced mail queue should be someone else's problem at 9pm, a managed cPanel host (HostOy markets exactly this; InterServer includes managed support from 8 slices) is worth the extra dollars.
- **You want zero license admin.** RackNerd makes you choose a license tier at checkout. If that decision sounds annoying rather than empowering, the bundled hosts remove it.
- **You need many locations or pay-as-you-go terms.** RackNerd's footprint is fixed at its listed data centers and the specials are annual. LightNode's hourly model across 40+ locations covers the opposite requirement.

## FAQ

**Do I need to buy WHM and cPanel separately?**
No. cPanel/WHM ships as one license — WHM is the server administration layer and cPanel is the per-account panel, and every tier from Solo upward includes both.

**How many websites can one license host?**
The license tier caps accounts: Solo is 1 account, Admin up to 30, Pro up to 100, Premium beyond that in expandable blocks. Inside each account, domain counts are limited by your disk and bandwidth rather than per-domain fees, which is why a single account can comfortably host several small sites.

**Which operating system should I pick for cPanel on a VPS?**
AlmaLinux 9. It's the current long-term-support default for new cPanel deployments, with Rocky Linux, CloudLinux, and Ubuntu LTS as valid alternatives depending on your needs.

**Can I move my existing cPanel accounts to a new VPS?**
Yes. WHM's built-in Transfer Tool copies accounts, email, and databases from another cPanel server. PingRack offers this as a free managed migration with downtime typically under five minutes per their FAQ; on an unmanaged RackNerd box you run the same transfer tools yourself, which is entirely doable if you can follow documentation.

## The short version before you order

If you're hosting one to five sites and don't mind owning the server admin work, the math consistently favors a RackNerd special plus the right license tier — the 2.5GB or 4GB plans cover most small hosting operations, and the renewal-price lock protects the deal for years. If you want managed support, CloudLinux out of the box, or more accounts than you want to think about, pick from the license-included column instead and pay for the convenience knowingly.

Two things to confirm before clicking buy on any of this: pick AlmaLinux 9 as the OS template (adding cPanel to the wrong OS is the most tedious mistake to undo), and match the license tier to your account count with headroom so you're not upgrading in month two.

- 👉 [Open RackNerd's current specials, choose your plan, and add the cPanel/WHM license tier that matches your account count](https://bit.ly/my-rn)
