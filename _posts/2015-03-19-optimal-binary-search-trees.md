---
layout: post
comments: True
title: Optimal Binary Search Trees
---

We are given a seqence $K = \langle k_1, \cdots, k_n \rangle$ of $n$ distinct keys in sorted order and we wish to build a binary search tree out of these keys. For each key, $k_i$, we have a probability $p_i$ that the search will be for $k_i$. Similarly, $d_0,\cdots, d_n$ represents values that are not in $K$. In particular, $d_0$ represents all values that are less than $k_1$, $d_i$ represents all values that are between $k_i$ and $k_{i+1}$. The dummy keys have corresponding probability $q_i$. So we have:

$$ \sum p_i + \sum q_i = 1.$$

The expected cost of a tree $T$ can thus be defined as

$$ E[\text{search cost in } T] = \sum(\text{depth}_T(k_i)+1) + \sum (\text{depth}_T(k_i)+1).$$

For a given set of probabilities, we wish to construct a binary search tree whose expected search time is the lowest. We call such a tree as **optimal binary search tree**.

**Note**:

* The optimal binary search tree *need not* be a tree with the smallest height.
* The optimal binary search tree *need not* be a tree with such that the node of highest probability occurs at the root.
* The brute force algorithm takes exponential time (the algorithm that calculate the expected search time of all such binary search trees).
* Dynamic programming is applicable, with the optimal substructure as sub-trees!






