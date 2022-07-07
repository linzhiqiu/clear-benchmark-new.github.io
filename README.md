---
description: By Carnegie Mellon University and CMU Argo AI Center
---

# The CLEAR Benchmark: Continual LEArning on Real-World Imagery



![](.gitbook/assets/banner\_white.png)

CLEAR is a novel continual/lifelong benchmark that captures real-world distribution shifts in Internet image collection (YFCC100M) from 2004 to 2014.&#x20;

> For long, researchers in continual learning (CL) community have been working with artificial CL benchmarks such as "Permuted-MNIST" and "Split-CIFAR", which do not align with practical applications. In reality, distribution shifts are smooth, such as natural temporal evolution of visual concepts.&#x20;

Below are examples of classes in [CLEAR-100](documentation/download-clear-10-clear-100.md) that changed over the past decade:

![Back to 2004, we had bulky desktop, old-fashioned analog watches, and 2D pixel-art game.
Nonetheless, visual concepts gradually evolved from 2004 to 2014, e.g., fancier-looking Macbook Pro, digital watches, and 3D realistic-graphics games.](.gitbook/assets/examples.png)

## About CLEAR Benchmark

The CLEAR Benchmark and the [CLEAR-10](documentation/download-clear-10-clear-100.md#clear-10-s3-download-links) dataset are first introduced in our [NeurIPS 2021 paper](https://arxiv.org/abs/2201.06289).&#x20;

{% embed url="https://arxiv.org/abs/2201.06289" %}
NeurIPS'21 Datasets and Benchmarks Track
{% endembed %}

In spirit of the famous [CIFAR-10/CIFAR-100 benchmarks](https://www.cs.toronto.edu/\~kriz/cifar.html) for static image classification tasks, we collected a more challenging [CLEAR-100](documentation/download-clear-10-clear-100.md#clear-100-s3-download-links) with a more diverse set of classes.

{% hint style="info" %}
We hope our [CLEAR-10/-100](documentation/download-clear-10-clear-100.md) benchmarks can be the new "CIFAR" as a test stone for continual/lifelong learning community.
{% endhint %}

We are also working to extend CLEAR to an ImageNet-scale benchmark. If you have feedback and insights, feel free to reach out to us!

{% content-ref url="introduction/about-us.md" %}
[about-us.md](introduction/about-us.md)
{% endcontent-ref %}



## 1st CLEAR challenge on CVPR 2022

In June 2022, the [1st CLEAR Challenge](https://www.aicrowd.com/challenges/cvpr-2022-clear-challenge) was hosted on [CVPR 2022 Open World Vision Workshop](https://www.cs.cmu.edu/\~shuk/vplow.html), with a total of 15 teams from 21 different countries and regions partcipating. You may find a quick summary of the workshop in below page:

{% content-ref url="introduction/1st-clear-challenge-cvpr22.md" %}
[1st-clear-challenge-cvpr22.md](introduction/1st-clear-challenge-cvpr22.md)
{% endcontent-ref %}

Given the top teams' promising performance on CLEAR-10/-100 benchmarks via utilizing methods that **improve** **generalization**, such as sharpness aware minimization, supervised contrastive loss, strong data augmentation, experience replay, etc., we believe there are still a wealth of problems in CLEAR for the community to explore, such as:

* Improving Forward Transfer and Next-Domain Accuracy
* Unsupervised Domain Adaptation/Generalization
* Self-supervised/Semi-Supervised Continous Learning
* Online Test-Time Adaptation

#### Note that this wiki page is under construction (as of July 7 2022)!

{% content-ref url="documentation/download-clear-10-clear-100.md" %}
[download-clear-10-clear-100.md](documentation/download-clear-10-clear-100.md)
{% endcontent-ref %}
