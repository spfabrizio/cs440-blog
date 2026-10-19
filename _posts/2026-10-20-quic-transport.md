---
layout: post
title: "Waiting for QUIC: Passive Measurements to Understand QUIC Deployments"
date: 2026-10-19
paper_authors: "J. Mücke, M. Nawrocki, R. Hiesgen, P. Sattler, J. Zirngibl, G. Carle, J. Luxemburk, T. C. Schmidt, M. Wählisch"
paper_venue: "CoNEXT 2025"
paper_url: "https://doi.org/10.1145/3768988"
week: 5
tags: [QUIC, measurement, load-balancing, infrastructure]
---

## Key Idea
QUIC has been designed for better performance and metadata privacy, but there is no certainty regarding how much information can still be extracted regarding infrastructure of large organizations. The authors perform passive analysis of QUIC backscatter traffic collected from the UCSD network telescope in order to analyze the deployments of various companies including Google, Meta, and Cloudflare from 2021 to 2025. It was found that packet features and connection IDs could help infer retransmission settings, off-net deployments, and even the number of layer 7 load balancers deployed by Meta.

## Critique
The approach is plausible because it considers actual traffic data spanning five years and confirms the results through both active and passive measurements. Nevertheless, backscatter traffic varies according to attacker behavior and is merely a representation of some of the servers deployed, so it is not possible to ascertain whether the observations are generalizable. Additionally, the capability to enumerate individual load balancers is shown for Meta alone.

## Connections
It has a connection with the paper from Week 1 because they both show how observable traffic patterns reflect the underlying architecture of the Internet. Moreover, it is connected to the paper on ECMP because they both speak about traffic distribution; however, in this case, we learn how QUIC connection IDs indicate load balancing infrastructure.
