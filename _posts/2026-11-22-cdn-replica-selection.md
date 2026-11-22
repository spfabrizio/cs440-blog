---
layout: post
title: "Who Holds the Steering Wheel? Opacity and Consolidation in CDN Replica Selection"
date: 2026-11-22
paper_authors: "R. Kumar, F. E. Bustamante, M. Flores"
paper_venue: "NINeS 2026"
paper_url: "https://doi.org/10.4230/OASIcs.NINeS.2026.23"
week: 10
tags: [CDN, replica-selection, DNS, anycast, network-measurement]
---
## Key Idea
Content Delivery Networks (CDNs) make use of replica selection for choosing servers from which content is delivered to users; however, the details about the selection process are generally not publicly available. The paper provides a new methodology for inferring which replica selection strategy is employed by a particular CDN and makes use of latency measurements collected by RIPE Atlas probes and geographically distributed DNS resolvers to distinguish between three main approaches used by CDNs: DNS-based redirection, global anycast, and regional anycast. With the help of latency distribution analysis, it is possible to infer the replica selection mechanism without accessing the CDN's internal infrastructure. The analysis of 17 CDNs across 19 countries reveals that DNS-based steering is still used by more than 70% of the CDNs studied.

## Critique
It appears to be reasonable since the research methodology is validated using well-known CDNs such as Akamai, Cloudflare, and Edgio prior to being used for a wider sample of CDNs. Nonetheless, only one RIPE Atlas probe is used in each country, thus possibly failing to provide a full understanding of how replicas are selected within the same country. Furthermore, the research concentrates on the landing pages of top-ranked websites, thus making it hard to determine if the results can be applied to other types of content, for instance, video streaming.

## Connections
This is related to the HiDe paper because they both deal with the effect of network routing decisions on Internet traffic in different geographical locations, but while the former is concerned with the detection of malicious BGP interception attacks, the latter deals with replica selection strategies for CDNs. This paper is also relevant to the OpenFLAME paper because both papers investigate the effect of naming and resolution mechanisms on the selection of network services.
