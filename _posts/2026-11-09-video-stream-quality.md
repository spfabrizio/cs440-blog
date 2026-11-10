---
layout: post
title: "Video Stream Quality Impacts Viewer Behavior: Inferring Causality Using Quasi-Experimental Designs"
date: 2026-11-09
paper_authors: "S. Shunmuga Krishnan, R. K. Sitaraman"
paper_venue: "IMC 2012"
paper_url: "https://doi.org/10.1145/2398776.2398799"
week: 8
tags: [video-streaming, CDN, viewer-behavior, causal-inference]
---

## Key Idea

In this study, the authors analyze the influence of video streaming quality on the behavior of viewers, including abandonment, engagement, and repeat viewership. As opposed to correlation analysis, the authors apply Quasi-Experimental Designs (QEDs) that allow comparing viewers with comparable characteristics and providing evidence of a causal relationship between changes in the quality of streaming and changes in behavior. Applying the data from 23 million video views, the authors establish that video abandonment starts when startup delay exceeds two seconds, with each extra second resulting in an increase in abandonment rates by 5.8%.

## Critique

The method is logical in the sense that the researchers study a large sample and consider factors such as content, connection type, and geography that act as confounders. However, the matching of viewers on the basis of such criteria does not fully rule out the effect of other variables that can influence their actions and makes it difficult to definitively establish causality. The second limitation relates to the fact that the data sample consists of ten days of on-demand video views.

## Connections

This is related to the LeoCC paper since both papers try to understand the effects of network performance on video streaming, even though the LeoCC paper seeks to improve throughput and reduce delay while this paper explores the effects of stream quality on viewer behavior. This paper is also related to the papers on congestion control since minimizing network congestion can improve streaming quality, which this paper links to viewer engagement.
