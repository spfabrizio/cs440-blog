---
layout: post
title: "OpenFLAME: A Federated Spatial Naming Infrastructure"
date: 2026-11-04
paper_authors: "S. Bharadwaj, Z. Ma, I. Liang, M. Farb, A. Rowe, S. Seshan"
paper_venue: "NINeS 2026"
paper_url: "https://doi.org/10.4230/OASIcs.NINeS.2026.20"
week: 7
tags: [spatial-naming, DNS, federated-mapping, privacy]
---

## Key Idea

The conventional map service providers like Google Maps and Apple Maps are based on centralized systems where the coverage is mainly restricted to outdoor areas, making it difficult to accommodate privacy concerns and provision of indoor maps. In order to overcome these issues, the authors introduce OpenFLAME, a federated spatial naming infrastructure, enabling each entity to maintain and serve its own maps. It is designed to use the existing DNS infrastructure and spatial indexing in order to find relevant map servers.

## Critique

This methodology seems plausible due to the use of OpenFLAME with the existing DNS infrastructure and the evaluation of the performance of this methodology against centralized mapping systems. The results demonstrate that federated routing takes roughly twice as long as centralized routing and yields longer routes, hence bringing to question the efficiency of this approach. Besides, the discovery method does not provide means for ranking map servers; therefore, it will be hard to choose proper maps from several providers in the same area.

## Connections

It ties in with the Week 1 paper in that both explore the impact that the design of Internet infrastructure has on application functionality. It ties in with the QUIC paper in that both pose privacy concerns with regard to networking technology, even though OpenFLAME concerns access control for spatial data and not information revealed by network traffic.

