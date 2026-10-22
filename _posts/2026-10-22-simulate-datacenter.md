---
layout: post
title: "Simulate Before Sending: Rethinking Transport in Datacenter Networks"
date: 2026-10-22
paper_authors: "D. Straussman, I. Keslassy, A. Shpiner, L. Liss"
paper_venue: "NINeS 2026"
paper_url: "https://doi.org/10.4230/OASIcs.NINeS.2026.19"
week: 5
tags: [datacenters, transport, congestion-control, AI-training]
---

## Key Idea
The AI training workload is known for its bursty nature in terms of data center network traffic, in which packet loss and retransmission may cause CCTs to increase considerably. The authors come up with the idea of dcSim as a new transport mechanism where small simulation packets (Sims) are first sent over candidate paths in the network and only after a Sim is acknowledged does the corresponding Data packet use the same path after a fixed delay.

## Critique
The methodology appears valid since the authors compare dcSim with other transport protocols in terms of varying workload scenarios, showing reduced CCTs and zero packet loss. Nevertheless, the study is based on simulations, which makes it challenging to establish whether the same findings will be applicable in a live data center environment. In addition, the authors admit that a successful Sim packet does not necessarily guarantee that the corresponding Data packet will avoid loss in multi-stage networks.

## Connections
This is relevant to the ECMP paper in that they both consider how traffic flow through different paths in the network may be optimized, although dcSim achieves this using simulation packets before Data transmission. This is also related to the in-network congestion signals paper since they both consider how network knowledge can affect transport performance, although dcSim achieves this through probing rather than congestion-based rate adjustment.
