---
layout: post
title: "Unlocking ECMP Programmability for Precise Traffic Control"
date: 2026-10-07
paper_authors: "Y. Liu, Y. Xiao, X. Zhang, W. Dang, H. Liu, X. Li, Z. He, J. Wang, A. Kuzmanovic, A. Chen, C. Miao"
paper_venue: "NSDI 2025"
paper_url: "https://www.usenix.org/conference/nsdi25/presentation/liu-yadong"
week: 3
tags: [ECMP, traffic engineering, data centers, reliability]
---

## Key Idea

The distribution of flows over equal-cost paths in ECMP is done through hashes, thus it is difficult to move a particular flow from a faulty or busy link. P-ECMP operates using the same ECMP groups along with a packet header selector, thereby allowing hosts to predictably change paths without having to replace regular ECMP.

## Critique

This paper is persuasive as it analyzes various use cases in simulation and provides findings from the live data center infrastructure of Tencent. In simulation, the P-ECMP algorithm reroutes flows in a single attempt, while in live data centers, storage I/O interruption time is shorter during failures. But only the failover use case is implemented in live data centers, making others less validated. Additionally, it requires an alternate route to be healthy and may require additional header bits for exact path control.

## Connections

This is similar to Raha in the sense that both of them deal with network failures; however, Raha looks for a combination of network failures and traffic that results in severe capacity reduction while P-ECMP deals with flow restoration. Another related paper is DCTCP; both react to congestion, but DCTCP adjusts sending rates while P-ECMP changes traffic paths.
