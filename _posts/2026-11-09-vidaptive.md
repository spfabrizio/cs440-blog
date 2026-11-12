---
layout: post
title: "Tight Loops, Smooth Streams: Responsive Congestion Control for Real-Time Video"
date: 2026-11-09
paper_authors: "P. Karimi, S. Fouladi, V. Sivaraman, M. Alizadeh"
paper_venue: "NINeS 2026"
paper_url: "https://doi.org/10.4230/OASIcs.NINeS.2026.9"
week: 8
tags: [real-time-video, congestion-control, WebRTC, latency]
---

## Key Idea

High video quality with low latency is mandatory for real-time video applications; however, current video rate controllers may not be able to react quickly in case of changes in network capacity. In this paper, Vidaptive is proposed as a framework, enabling real-time video to leverage existing congestion control algorithms (CCAs) without modifying existing video codecs. Vidaptive decouples video encoding from packet transmission and sends dummy packets to maintain a tight feedback loop. It also dynamically adjusts the encoder's target bitrate based on measured frame service times to ensure a trade-off between video quality and frame latency.

## Critique

This seems like a plausible technique since the authors implement their framework in WebRTC and evaluate the performance of Vidaptive as compared to existing rate controllers through the use of cellular network traces. The only problem with their experiment is that it involves mostly emulated network conditions and thus it becomes difficult to gauge the performance of the framework in live network deployments. Moreover, the dummy packets also consume bandwidth and might increase battery consumption.

## Connections

This is relevant to the LeoCC research paper in that both use responsive congestion control to adapt to network changes while maintaining low latency. While LeoCC is designed for satellite network dynamics, Vidaptive aims to improve video quality and reduce latency in real-time video streams. It is also related to the paper about video stream quality since both highlight the importance of quality, albeit from different angles.
