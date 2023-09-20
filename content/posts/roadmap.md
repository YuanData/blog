---
title: "Roadmap"
date: 2023-09-20T07:00:00+08:00
draft: false
tags: ["LeetCode"]
---
### Roadmap
此流程圖描繪了從基礎技術如陣列和雜湊，逐步深入到更專業、高階的技術領域，如數學和幾何等技術的學習路徑。

1. 陣列和雜湊 (Arrays and Hashing)：
   - 雙指針 (Two Pointers)
   - 堆疊 (Stack)

2. 雙指針 (Two Pointers) 技術可以再進一步細分為：
   - 二分搜尋 (Binary Search)
   - 滑動窗口 (Sliding Window)
   - 鏈結列表 (Linked List)

3. 樹 (Trees)：
   - 字典樹 (Tries)
   - 堆積或優先隊列 (Heap or Priority Queue)
   - 回溯 (Backtracking)

4. 回溯 (Backtracking)：
   - 圖 (Graphs)
   - 一維動態規劃 (1-space Dynamic Programming)

5. 堆積或優先隊列 (Heap or Priority Queue)：
   - 區間 (Intervals)
   - 貪婪 (Greedy)
   - 進階圖形 (Advanced Graphs)

7. 一維動態規劃 (1-space Dynamic Programming)：
   - 二維間動態規劃 (2-space Dynamic Programming)
   - 位元操作 (Bit Manipulation)
   - 數學和幾何 (Math and Geometry)

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
