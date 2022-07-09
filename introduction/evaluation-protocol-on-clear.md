---
description: How to faithfully evaluate a continual learning algorithm on CLEAR?
---

# Evaluation Protocol on CLEAR

For bucket 1st to 10th that each comes with an annotated labeled trainset, we also release **a held-out testset** over the same timespan (now downloadable [here](../documentation/download-clear-10-clear-100.md)).&#x20;

Evaluating on CLEAR is the same as on any other continual learning benchmarks: we measure the performance of a model per timestamp on all the 10 testsets. This produces a _10x10 accuracy matrix_.

Different parts of the accuracy matrix focus on different aspects of the performance of a model. For example, the diagonal entries represent performance on a testset that is sampled from the same distribution as the current bucket (assuming each bucket is a locally iid distribution). Lower triangular part of the matrix instead focus on test performance on previously seen buckets, which is the focus of most state-of-the-art works combatting the forgetting issue. Therefore, we introduce 4 simplified evaluation metrics to summarize the accuracy matrix:

![A visual illustration of the 4 evaluation metrics on a 4x4 accuracy matrix.](../.gitbook/assets/content\_metrics.png)

1. `In-Domain Accuracy:` The average of diagonal entries, i.e., test performance _within the same_ _domain_ of current bucket.
2. `Next-Domain Accuracy:` The average of super-diagonal entries, i.e., test performance on the _immediate next domain_.
3. `Backward Transfer:` The average of lower triangular entries, i.e., test performance on _previously seen domains_.
4. `Forward Transfer:` The average of upper triangular entries, i.e., test performance on _future unseen domains_.

We hope that our proposed metrics can simplify evaluation on CLEAR and similar domain-incremental benchmarks; nonetheless, CLEAR can also be repurposed for task-/class-incremental scenarios, which could be exciting future works.
