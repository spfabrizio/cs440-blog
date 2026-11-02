---
layout: post
title: "DistTrain: Addressing Model and Data Heterogeneity with Disaggregated Training for Multimodal Large Language Models"
date: 2026-10-29
paper_authors: "Z. Zhang, Y. Zhong, Y. Jiang, H. Hu, J. Sun, Z. Ge, Y. Zhu, D. Jiang, X. Jin"
paper_venue: "SIGCOMM 2025"
paper_url: "https://doi.org/10.1145/3718958.3750472"
week: 6
tags: [AI-training, multimodal-LLMs, distributed-training, GPU-utilization]
---

## Key Idea

Multimodal LLM training poses problems owing to varying computational needs of different model components and data modalities leading to inefficient GPU usage. DistTrain is a proposed distributed system to train multimodal LLMs by decoupling the encoder, the LLM backbone, and the generator to have separate GPU resource allocation and parallelism techniques. Moreover, DistTrain decouples the data pre-processing phase from the training process and orders the training samples to minimize the stragglers and pipeline bubbles. DistTrain has up to 2.2x higher training throughput than Megatron-LM.
## Critique

The technique is convincing since the researchers run DistTrain on a production cluster having over a thousand GPUs and make comparison with Megatron-LM performance at different model scales. Nonetheless, the experiments are conducted only on image and text data; thus, it becomes hard to say if the results will be replicable for other types of data like audio and video. Besides, there is less difference in performance for the largest model; therefore, the question arises of what more can DistTrain offer as the model size increases.

## Connections

This has to do with the dcSim paper in that it seeks to enhance the efficiency of AI training workload processes although the dcSim is geared towards the reduction of packet losses. This also has to do with the RDMA reliability paper in that efficient network communication is necessary in distributed training although the DistTrain paper mainly deals with resource allocation.
