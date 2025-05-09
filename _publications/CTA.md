---
title: "Cta: Hardware-software co-design for compressed token attention mechanism"
collection: publications
category: conferences
permalink: /publication/CTA
excerpt: 'Proposing an accelerator with token compression for attention encoding'
date: 2023-02-25
venue: 'IEEE International Symposium on High-Performance Computer Architecture (HPCA)'
slidesurl: '/files/CTA_slides.pdf'
paperurl: '/files/CTA.pdf'
citation: 'Wang H, Xu H, Wang Y, et al. Cta: Hardware-software co-design for compressed token attention mechanism[C]//2023 IEEE International Symposium on High-Performance Computer Architecture (HPCA). IEEE, 2023: 429-441.'
videourl: 'https://www.youtube.com/watch?v=eVz77qGkbEU'
---
Abstract:
The attention mechanism is becoming an integral part of modern neural networks, bringing breakthroughs to Natural Language Processing (NLP) applications and even Computer Vision (CV) applications. Unfortunately, the superiority of attention mechanism comes from its ability to model relations between any two positions in long sequence, which incurs high inference overhead. For state-of-the-art AI workloads such as Bert or GPT-2, attention mechanism is reported to account up to 50% of the inference overhead. Previous works seek to alleviate this performance bottleneck by removing useless relations for each position and accelerate position-specific operations. However their attempts require selecting from a sequence of relations once for each position, which is essentially frequent on-the-fly pruning and breaks the inherent parallelism in attention mechanism. In this paper, we propose CTA, an algorithm-architecture co-designed solution that can substantially reduce theoretic complexity of attention mechanism, enabling significant speedup and energy saving. Inspired by the fact that the feature sequence encoded by attention mechanism contain a large number of semantic feature repetition, we propose a novel approximation scheme that can efficiently remove that repetition, only calculating attention among necessary features thus reducing computation complexity quadratically. To utilize this algorithmic bonus and empower high performance attention mechanism inference, we devise specialized architecture to efficiently support the proposed approximation scheme. Extensive experiments show that, on average, CTA achieves 27.7× speedup, 634.0× energy savings with no accuracy loss, and 44.2× speedup, 950.0× energy savings with around 1% accuracy loss over Nvidia V100-SXM2 GPU. Also, CTA achieves 22.8× speedup, 479.6× energy savings over ELSA accelerator+GPU system.