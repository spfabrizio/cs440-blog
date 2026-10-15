---
layout: post
title: "No Signal to Rule Them All: A Systematic Analysis of In-Network Congestion Signals"
date: 2026-10-14
paper_authors: "S. McClure, N. Dukkipati, S. Ratnasamy, S. Shenker"
paper_venue: "NINeS 2026"
paper_url: "https://doi.org/10.4230/OASIcs.NINeS.2026.12"
week: 4
tags: [congestion-control, telemetry, datacenters, INT]
---

## Key Idea
Datacenter congestion control has been able to take advantage of in-network telemetry (INT), but it is unclear whether having more detailed information about routers can improve performance compared to traditional end-to-end signals. For that reason, the authors used R+, a modified learning-based congestion control generator, and compared the resulting algorithms across different signals and performance objectives. They found that INT-based and end-to-end-only controllers achieve almost equivalent average performance, within 3% of each other.
## Critique
The comparison appears credible since the authors produce a separate controller for each set of signals and do not favor any specific approach, while the primary finding is supported through modifications to BBR. Yet the majority of experiments conducted use simulation techniques and simplified networks, which makes the conclusions hard to apply in practice to production datacenters. Moreover, concentrating on average throughput and delay can make researchers overlook some of the other potential benefits, such as improvements in tail latency.
## Connections
This relates to DCTCP, which employs ECN markings as network feedback, by raising the question of how much additional feedback is necessary for a congestion controller. Moreover, it relates to the ECMP paper: while P-ECMP changes the paths that traffic flows use, this paper considers what kind of signals would be suitable for adjusting their sending rates.
