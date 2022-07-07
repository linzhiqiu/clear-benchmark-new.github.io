---
description: By Carnegie Mellon University and CMU Argo AI Center
---

# The CLEAR Benchmark: Continual LEArning on Real-World Imagery



![](.gitbook/assets/banner\_white.png)

CLEAR is a novel continual/lifelong benchmark that captures real-world distribution shifts in Internet image collection (YFCC100M) from 2004 to 2014.&#x20;

> For long, researchers in continual learning (CL) community have been working with artificial CL benchmarks such as "Permuted-MNIST" and "Split-CIFAR", which do not align with any practical applications. In reality, distribution shifts are smooth, such as natural temporal evolution of visual concepts.&#x20;

Below are examples of classes in [CLEAR-100](documentation/download-clear-10-clear-100.md) that changed over the past decade:

![Back to 2004, we had bulky desktop, old-fashioned analog watches, and 2D pixel-art game.
Nonetheless, visual concepts gradually evolved from 2004 to 2014, e.g., fancier-looking Macbook Pro, digital watches, and 3D realistic-graphics games.](.gitbook/assets/examples.png)

## About CLEAR Benchmark

The CLEAR Benchmark is first introduced in a NeurIPS 2021 paper (Datasets and Benchmarks Track), as well as the CLEAR-10 dataset.&#x20;

In spirit of the famous CIFAR-10/CIFAR-100 benchmarks for static image classification tasks, we expanded to a more challenging version: CLEAR-100, with a more diverse set of 100 classes.

In June 2022, the 1st CLEAR Challenge was hosted on CVPR 2022 Open World Vision Workshop, with a total of 15 teams from 21 different countries and regions partcipating. \


Despite that the top teams achieved high scores on the current CLEAR benchmarks, we believe there are still a wealth of problems in CLEAR for the community to explore, such as:

* Improving Forward Transfer and Next-Domain Accuracy
* Continual Domain Adaptation/Generalization
* Self-supervised/Semi-Supervised Continous Learning
* Online Test-Time Adaptation

#### Note that this wiki page is under construction (as of July 7 2022)!

{% content-ref url="documentation/download-clear-10-clear-100.md" %}
[download-clear-10-clear-100.md](documentation/download-clear-10-clear-100.md)
{% endcontent-ref %}
