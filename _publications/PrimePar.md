---
title: "PrimePar: Efficient Spatial-temporal Tensor Partitioning for Large Transformer Model Training"
collection: publications
category: conferences
permalink: /publication/PrimePar
excerpt: 'Parallelism optimization for LLM training: a novel angle of hiding communication latency'
date: 2024-04-27
venue: 'ASPLOS24: the 29th ACM International Conference on Architectural Support for Programming Languages and Operating Systems'
slidesurl: '/files/primepar_slides.pdf'
paperurl: '/files/primepar.pdf'
citation: 'Wang H, Wang L, Xu H, et al. Primepar: Efficient spatial-temporal tensor partitioning for large transformer model training[C]//Proceedings of the 29th ACM International Conference on Architectural Support for Programming Languages and Operating Systems, Volume 3. 2024: 801-817.'
videourl: 'https://www.youtube.com/watch?v=q1HmUO9Al6Q'
---
Abstract:
With the rapid up-scaling of transformer-based large language models (LLM), training these models is becoming increasingly demanding on novel parallel training techniques. Tensor partitioning is an extensively researched parallel technique, encompassing data and model parallelism, and has a significant influence on LLM training performance. However, existing state-of-the-art parallel training systems are based on incomplete tensor partitioning space, where the distribution of partitioned sub-operators is limited to the spatial dimension. We discover that introducing the temporal dimension into tensor partitioning of LLM training instance provides extra opportunities to avoid collective communication across devices, saving memory space and also overlapping device-to-device communication with computation. In this paper, we propose a new tensor partition primitive that distributes sub-operators along both the spatial and temporal dimensions to further explore communication and memory overhead reduction over current solutions. This new primitive creates a broader parallelization space and leads to parallel solutions that achieve better training throughput with lower peak memory occupancy compared to state-of-the-art techniques. To efficiently deploy optimized parallel transformer model training to multiple devices, we further present an optimization algorithm that can find optimal parallel solutions from our spatial-temporal tensor partition space with acceptable search time. Our evaluation shows that our optimized tensor partitioning achieves up to 1.68 × training throughput with 69% peak memory occupancy compared to state-of-the-art distributed training systems when training LLMs. Upon scaling to 32 GPUs, the geo-mean speedup across benchmarks is 1.30 ×. When applied in 3D parallelism, up to 1.46 × training throughput can be achieved.