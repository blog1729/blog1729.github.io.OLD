---
layout: post
title: Huffman Codes
comments: True
---

Firstly, this is an example of a greedy algorithm. We can represent data in files by using **binary character code** in which each character is represented by a unique binary string, which we call as a **codeword**. We may use a **fixed-length code** or a **variable-length** code. Typically, **variable-length** code is minimizes the amount of data required to store a file.

## Prefix Codes

In this case, no codeword is a prefix of another (and hence the name prefix codes). *One can show that a prefix code can always achieve the optimal data compression among any character code.* Since no code is a prefix of another, decoding is easy---read the code till you get a match.

We see that a binary tree whose leaves are the given characters provide a nice representation of prefix codes. The binary representation of the prefix code can be interpreted in the following way: if a one is found it means to go to the right child and if a zero is found, go to the left child.

*One can show that  an optimal code for a file is a always represented by a full binary tree* (a **full binary tree** is a tree in which every non-leaf node has two children).

*If $C$ is the alphabet from which characters are drawn, and all character frequencies are positive, then the tree for an optimal prefix code has exactly $\vert C\vert$ leaves, one for each letter of the alphabet and exactly $\vert C\vert -1$ internal nodes.*

Given a tree $T$ corresponding to a prefix code, we can compute the number of bits required to encode a file. For each character $c$ in the alphabet $C$, let $c.freq$ denote the frequency of $c$ in the file and $d_T(c)$ denote the depth of $c$'s leaf in the tree. Thus the number of bits required to encode a file is thus

$$B(T) = \sum_{c\in C} c.freq \cdot d_T(C)$$

## Constructing a Huffman code

The algorithm proceeds as follows

* It first selects the two elements with minimum frequency, combines the two of them (virtually) and then (virtually) adds them into the list with frequency of the added element being the sum of the two elements initially selected. The added element can be visualized as a tree the leaf nodes being the two elements selected and the node contains the sum of frequencies of the two leaf elements.
* The above process is repeated until there are no elements left in the list.

Let the list, we referred to in the last paragraph be $Q$, we use a min-heap to model the list. The running time will then be $\mathcal O (n\lg n)$, where there are $n$ calls to the $Q$ and at each call, `BUILD-MIN-HEAP` is to be called. The correctness of the algorithm, of course, can be proved, but is omitted for trivial reasons.

## Notes

* The same algorithm can be used for a ternary prefix code, where the tree shall have three nodes (I am told that this will work).
* If the frequencies of the alphabet are Fibonacci numbers, then the tree has a particularly simple, predictable form.
* One can show that a binary tree that is not full cannot correspond to an optimal prefix code.







