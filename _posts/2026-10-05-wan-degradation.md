---
layout: post
title: "How Bad Can WAN Failures Really Get?"
date: 2026-10-06
paper_authors: "B. Arzani, S. Taheri, P. Namyar, R. Beckett, S. K. R. Kakarla, E. Jallilipour"
paper_venue: "SIGCOMM 2025"
paper_url: "https://doi.org/10.1145/3718958.3754348"
week: 3
tags: [WAN, traffic engineering, reliability, optimization]
---

## Key Idea

Some of the failure scenarios found in WANs, namely multiple link failures and changing traffic demands, can cause serious degradation, yet existing tools may not capture them. The proposed approach to solving this problem is to consider arbitrary probable failures, variable traffic demands, and degradation relative to the healthy network’s design point.

## Critique

This paper is very convincing in terms of Raha being evaluated on both Microsoft's production WAN and on topologies of public networks, hence demonstrating that the technique works even outside small-scale instances. Nonetheless, scalability may require approximations, such as clustering, that may sacrifice optimality in favor of more efficient runtimes. Moreover, the analysis relies on an estimation of link failure probabilities, which may influence the selection of significant scenarios by Raha.

## Connections

This is related to the partial reachability paper since both demonstrate the problems associated with simplification of network failure modes to just a few types. Partial reachability does not take for granted that networks are either up or down, whereas Raha does not accept the notion that it is sufficient to test just a few failures.
