---
layout: post
title: "What Does It Mean for the Internet to Be Up?"
date: 2026-09-30
paper_authors: "G. Baltra, T. Saluja, Y. Pradkin, J. Heidemann"
paper_venue: "NINeS 2026"
paper_url: "https://nines-conference.org/papers/p004-Baltra.pdf"
week: 2
tags: [routing, reachability, BGP, measurement]
---

## Key Idea

Typically, Internet disruptions have been classified into one of two categories, that is, either a network is reachable or not. In this research paper, the authors have proposed that there exists a category that has not been really explored: partial reachability, where peninsulas represent those networks that are reachable only from a certain portion of the Internet core while islands refer to the rest of the networks which are disconnected from the core but can still communicate with themselves.

## Critique

The claim proposed is very reasonable since the authors have demonstrated their approach in various systems and explained how three independent vantage points provide reliable results. Attribution is less reasonable. First, peninsulas can be consistent with routing policy disputes, but such a conclusion cannot determine the cause. Second, the term is IP-layer-based, meaning that "reachable" does not always mean availability of a working application for the user.

## Connections

While Gao-Rexford demonstrated how local routing rules can ensure global stability without any central planning, this paper highlights the flipside of that approach; that is, even stable routing need not lead to uniform reachability. This relates to the Week 1 post as both papers highlight how persistent behavior on the Internet reveals its underlying architecture.
