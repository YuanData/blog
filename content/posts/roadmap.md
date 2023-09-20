---
title: "Roadmap"
date: 2023-09-20T07:00:00+08:00
draft: false
---
### Roadmap
{{< mermaid >}}
flowchart TD
    1(Arrays and Hashing)
    1 --> 2_1(Two Pointers)
    1 --> 2_2(Stack)

    2_1 --> 3_1(Binary Search)
    2_1 --> 3_2(Sliding Window)
    2_1 --> 3_3(Linked List)

    3_1 --> 4(Trees)
    3_3 --> 4

    4 --> 5_1(Tries)
    4 --> 6_1(Heap or Priority Queue)

    6_1 --> 7_1(Intervals)
    6_1 --> 7_2(Greedy)
    6_1 --> 7_3(Advanced Graphs)

    4 --> 5_2(Backtracking)
    5_2 --> 6_2(Graphs)
    6_2 -->7_3

    5_2 --> 6_3(1-space Dynamic Programming)
    6_3 --> 7_4(2-space Dynamic Programming)
    6_2 -->7_4
    6_3 --> 7_5(Bit Manipulation)

    7_5 --> 8(Math and Geometry)
    6_2 -->8
{{< /mermaid >}}
reference: neetcode.io
