# Buy VPS Windows: Which Plan Runs Your Apps, What the Licence Adds, and How Many People Can Log In at Once (Full SpinServers Plan Table)

SpinServers sells KVM VPS from **$12/month**: 2 vCPU, 2 GB RAM, 40 GB RAID-10 SSD and 4 TB of transfer on a 1 Gbps port, billed month to month with no setup fee. Windows is not in that number. The plans are self-managed with root access, and no Windows template or licence add-on appears on the plan pages, so you supply the operating system licence and should get support to confirm your install path in writing before you pay. If you are shopping to buy VPS Windows capacity for one application, the 4 vCPU / 4 GB build at **$29** is usually the better buy than the $12 tier, because Windows Server itself will eat most of 2 GB.

Below: the full plan ladder, what a licence adds over twelve months, how many people can actually be logged in at once, and which of their two US data centres to pick.

> **Quick pick**
> - One trading terminal or a single accounting package, one user: **4 vCPU / 4 GB at $29/mo**
> - SQL Server Express plus IIS, two or three RDP users: **6 vCPU / 8 GB at $39/mo**
> - Testing an installer before committing: **2 vCPU / 2 GB at $12/mo**, and expect to fight the RAM ceiling
> - 👉 [See the current SpinServers KVM VPS plans and monthly prices](https://bit.ly/Spinservers)

## SpinServers VPS plans and prices

All prices in USD, billed monthly, no setup fee. Every plan includes one IPv4 and one IPv6 address, a 1 Gbps port, root access, and port 25 closed by default.

| Plan | vCPU · RAM · Storage | Transfer / port | Price (USD/mo) | Order |
| --- | --- | --- | --- | --- |
| KVM 2 | 2 vCPU · 2 GB DDR4 · 40 GB RAID-10 SSD | 4 TB · 1 Gbps | **$12** | [Deploy the 2 vCPU plan](https://bit.ly/Spinservers) |
| KVM 4 | 4 vCPU · 4 GB DDR4 · 80 GB RAID-10 SSD | 8 TB · 1 Gbps | **$29** | [Deploy the 4 vCPU plan](https://bit.ly/Spinservers) |
| KVM 6 | 6 vCPU · 8 GB DDR4 · 120 GB RAID-10 SSD | 8 TB · 1 Gbps | **$39** | [Deploy the 6 vCPU plan](https://bit.ly/Spinservers) |
| KVM 8 | 8 vCPU · 8 GB DDR4 · 160 GB RAID-10 SSD | 10 TB · 1 Gbps | quoted per build | [Configure the 8 vCPU build](https://bit.ly/Spinservers) |
| KVM 12 | 12 vCPU · 12 GB DDR4 · 160 GB SSD | 10 TB · 1 Gbps | from **$62** | [Configure the 12 vCPU build](https://bit.ly/Spinservers) |
| KVM 16 | 16 vCPU · 16 GB DDR4 · 320 GB RAID-10 SSD | 15 TB · 1 Gbps | quoted per build | [Configure the 16 vCPU build](https://bit.ly/Spinservers) |
| KVM 32 | 32 vCPU · 32 GB · 500 GB SSD | 20 TB · 1 Gbps | quoted per build | [Configure the 32 vCPU build](https://bit.ly/Spinservers) |

Anything from 8 vCPU upward is built to order rather than sold off a fixed price card, and the configurations in that range are the ones most likely to be out of stock. If you need a specific core count, order when you are ready to configure rather than a month ahead.

## What the monthly price leaves out: the Windows licence

Nothing on the SpinServers plan page bundles a Windows Server licence, and no licence shows up in the add-on list. Treat the OS as your purchase, and get a ticket on record confirming that you can mount your own Windows ISO and activate with your own key before you commit to a long-running build.

Hosts that do sell Windows split into three pricing models, and the spread is wide enough to change which plan you can afford:

- **Evaluation first, per-vCPU after.** MassiveGRID installs Windows Server as a 180-day evaluation. After day 180 the machine keeps your files but is shut down every hour until a licence is attached, charged at $6.31 per vCPU. A 2 vCPU server therefore carries $12.62/month on top of the sticker.
- **Flat monthly add-on.** HostFinch lists Windows Server 2019 Standard and 2016 Standard at $19.99/month each, with 2022 Standard quote-only.
- **Desktop Windows on your own key.** Microsoft does not let hosting companies rent Windows 10 or 11 Pro. Those templates arrive unactivated and you type in your own product key. Windows 11 Pro also needs at least 2 GB of RAM, which is why desktop configurations start there.

Over twelve months the arithmetic gets uncomfortable. The $12 SpinServers slice is $144 for the year. Add a 2 vCPU licence at MassiveGRID's rate and you are at roughly $295; take HostFinch's flat $19.99 add-on instead and you are near $384. Hardware is the cheap half of a Windows server.

Two licensing details catch people out. Windows 10 reached end of support on 14 October 2025 and no longer receives security updates, so new builds belong on Windows 11 Pro or Windows Server. Windows Server 2025 is the current default image at most providers, with 2016, 2019 and 2022 kept for applications that have not been certified on the newer release.

👉 [Compare SpinServers tiers against the cost of the licence you need](https://bit.ly/Spinservers)

## How many people can log in at once

Two, on Windows Server, and that is the ceiling until you buy more.

Two administrative RDP sessions is the standard allowance across the Windows hosts reviewed here. MassiveGRID charges $8.90 per additional user per month; HostFinch quotes extra RDP CALs case by case. SpinServers publishes no CAL pricing at all, so if three or more people need to be connected simultaneously, price the CALs separately and add that figure to whichever plan you choose. A CAL is a Microsoft licence, not a hosting feature, and no plan size removes the need for it.

Desktop editions are stricter still. Windows 10 and 11 Pro allow a single interactive session, so a small team cannot share one. The moment a second person connects at the same time, the operating system has to be Windows Server.

For a single user, the 4 vCPU / 4 GB plan at $29 is a sensible home for a MetaTrader terminal or a desktop accounting package. InterServer advises starting MetaTrader workloads at 4 slices, which on its platform means 2 cores and 8 GB, so 4 GB is on the lean side if you plan to run several expert advisors at once. Move to the 6 vCPU / 8 GB plan at $39 in that case.

👉 [Start with the $39 6 vCPU plan if two or three people will connect](https://bit.ly/Spinservers)

## Where the server sits, and why RDP feels it

SpinServers operates two facilities: Dallas, Texas and San Jose, California. Both are Tier III, SOC2, HIPAA and PCI compliant, running on their own ASN (396073) with Cogent, HE, Level 3 and IX transit. A Windows desktop in a browser window is latency-sensitive in a way a Linux web server is not, since every keystroke and window drag makes the round trip. Dallas suits users east of the Rockies and into Latin America; San Jose suits the West Coast and connections across the Pacific.

Port 25 is closed by default on every VPS, and you need a ticket with a justification to get it opened. Anything that sends mail over SMTP, including alerting scripts and older line-of-business applications, has to clear that on day one. InterServer runs the same policy, so it is an industry habit rather than a quirk, but it is the sort of thing you find out after the server is live.

Deployment is quoted at around 30 minutes. The recurring caveat in third-party write-ups is stock rather than speed: popular configurations sell out, and what is listed today may not be listed next week.

Above the VPS line, the company's main business is bare metal, from $79/month for a Xeon E3-1280 v5 with 32 GB RAM, 1 TB NVMe and 30 TB of transfer on dual 10 Gbps ports. On bare metal the Windows licence is entirely your own arrangement, which makes it the cleaner route once one VM stops being enough for your database or your user count.

## How the Windows VPS market prices out

Same job, very different bills. The table below uses each provider's cheapest verified Windows-capable configuration rather than its headline starting price, because a $3.99 plan and a $29.40 plan are rarely the same product.

| Provider | Entry Windows configuration | Price | Licence handling |
| --- | --- | --- | --- |
| SpinServers | 2 vCPU / 2 GB / 40 GB SSD / 4 TB, self-managed KVM | $12/mo | No licence line item; bring your own |
| MassiveGRID | 1 vCPU / 2 GB / 32 GB NVMe (Windows 11 Pro); 1 GB on Server Starter | $4.79/mo; $3.99/mo | 180-day evaluation, then $6.31 per vCPU |
| HostFinch | 1 vCPU / 2 GB / 40 GB SSD, US location | $12.99/mo | Server 2019 or 2016 Standard +$19.99/mo |
| Contabo | 6 vCPU / 12 GB / 200 GB SSD, 200 Mbit/s port, unlimited traffic | $29.40/mo | Windows Server image preinstalled |
| InterServer | 8 cores / 32 GB / 640 GB SSD / 32 TB (16 slices, Hyper-V) | $80/mo | Windows VPS platform; 2-slice minimum |

Read the licence column before the price column. The $3.99 and $4.79 entries are real, but they are 1 to 2 GB machines where the evaluation clock is running, and a 1 GB Windows Server is a configuration you outgrow in a week. Contabo's CLOUD VPS 6 is the sharper deal on paper at the six-core mark: more RAM than the SpinServers KVM 6 for less money, with Windows already installed. SpinServers answers with US placement in two named cities, a 1 Gbps port on every plan, and the option to keep scaling to 32 vCPU on the same platform.

## Who this is wrong for

Two groups, honestly.

Anyone running a Linux stack, a static site or a container workload should not pay the Windows premium at all. The licence either adds a monthly line or starts an evaluation countdown, and neither buys you anything if nginx would have done the job. Worth knowing before you pick a host: IONOS states that once you choose a Windows virtual server you cannot switch that machine to Linux later, and you have to place a new order instead. SpinServers sells self-managed KVM where the OS is your install, but the general lesson holds, since plenty of hosts lock the image at order time.

Anyone who wants the licence inside the monthly fee and a managed hand on the OS should look at the hosts that bundle it. A preinstalled Windows Server image with support included is a different product from a bare KVM slice, and the price difference reflects that.

## Before you order

Pick by what has to run, not by what looks cheap:

- **One trading terminal or one accounting package, single user:** 4 vCPU / 4 GB at $29. Below that, Windows Server leaves you too little headroom.
- **.NET app with SQL Server Express, two or three RDP users:** 6 vCPU / 8 GB at $39, and plan the move to 16 GB when the database file passes a few gigabytes.
- **Five or more people connected at once:** price the RDS CALs first. They will likely cost more per year than the server, and no plan size changes that.
- **Heavy MSSQL or a farm of bots running at full CPU for hours:** skip the VPS line and take a dedicated box at $79, where you own the cores and the licence question is entirely yours.

Three things to settle in a ticket before you pay. Confirm that installing Windows with your own key on the KVM plan is acceptable and that you can attach an ISO. Confirm the rate holds on renewal, since the plans are month to month and a wrong guess costs one billing period rather than a year. And confirm current stock on the core count you want, because the larger builds are made to order.

👉 [Check availability and current pricing on the SpinServers VPS range](https://bit.ly/Spinservers)
