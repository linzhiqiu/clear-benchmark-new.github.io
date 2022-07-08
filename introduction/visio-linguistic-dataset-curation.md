---
description: How to efficiently annotate a million-scale Internet image collection?
cover: >-
  https://images.unsplash.com/photo-1519389950473-47ba0277781c?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=2970&q=80
coverY: 0
---

# Visio-Linguistic Dataset Curation

We start from the public [YFCC100M](http://projects.dfki.uni-kl.de/yfcc100m/) collection that contains Flickr images uploaded between 2004 and 2014. We downloaded a 8M subset for building CLEAR-10, and a 40M subset for building CLEAR-100.

We use the **upload timestamps** to recreate the temporal stream and split the 8M/40M into **11 buckets of images**, each spanning on average one year of data. The 0th bucket is reserved for unsupervised pre-training (e.g., MoCo), and we curate a small but **high-quality labeled set** (with CLEAR-10 and CLEAR-10 ontology defined [here](about-clear-benchmark.md#temporal-evolution-of-visual-concepts)) for **each of the 1st to 10th buckets**.&#x20;

To avoid excessive human annotation cost on web-scale data, we use the visio-linguistic dataset curation approach proposed in our [NeurIPS'21 paper](https://arxiv.org/pdf/2201.06289.pdf). The key idea is to leverage OpenAI's recent [CLIP](https://openai.com/blog/clip/) model and prompt engineering techniques for efficient image retrieval. The top-scoring images retrieved by CLIP are later verified by human annotators to ensure 99% precision (crowdsourced [MTurk](https://www.mturk.com) workers for CLEAR-10 and c[ommericial labelling service](https://stardust-ai.com) for CLEAR-100).

The entire pipeline can be summarized:

![](../.gitbook/assets/dataset.png)
