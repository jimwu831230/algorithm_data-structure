# Algorithm & Data Structure

## LeetCode

* [Queue & Stack](https://leetcode.com/explore/learn/card/queue-stack/)
  * [circular queue](LeetCode/QueueStack/circularQueue.cpp)

## Links

* [Mastering Markdown · GitHub Guides](https://guides.github.com/features/mastering-markdown/)
  * [Markdown Cheatsheet 中文版](https://gist.github.com/billy3321/1001749662c370887c63bb30f26c9e6e)

## Sorting Algorithm 排序算法
* 
|  排序算法               | 平均複雜度  | 最壞情況     | 空間複雜度 | 排序方式   |
| :--------------------: | :--------: | :----------: | :-------: | :-------: |
| 冒泡排序 Bubble sort    | $O(n^2)$   | $O(n^2)$     | $O(1)$    | In-place  |
| 選擇排序 Selection sort | $O(n^2)$   | $O(n^2)$     | $O(1)$    | In-place  |
| 插入排序 Insertion sort | $O(n^2)$   | $O(n^2)$     | $O(1)$    | In-place  |
| 希爾排序 Shell sort     | $O(nlogn)$ | $O(nlog^2n)$ | $O(1)$    | In-place  |
| 歸併排序 Merge sort     | $O(nlogn)$ | $O(nlogn)$   | $O(n)$    | Out-place |
| 快速排序 quick sort     | $(nlogn)$  | $O(n^2)$     | $O(logn)$ | In-place  |
| 推排序 Heap sort        | $O(nlogn)$ | $O(nlogn)$   | $O(1)$    | In-place  |
| 計數排序 Counting sort  | $O(n+k)$   | $O(n+k)$     | $O(k)$    | Out-place |
| 桶排序 Bucket sort      | $O(n+k)$   | $O(n^2)$     | $O(n+k)$  | Out-place |
| 基數排序 radix sort     | $O(n+k)$   | $O(nxk)$     | $O(n+k)$  | Out-place |
 
 * n: 代表數據規模及數據量大小
   k: 桶的個數
   In-place: 不佔用額外內存，只佔用常數內存
   Out-place: 佔用額外內存

  * Bubble sort 冒泡排序法
   * Bubble sort is a simple sorting algorithm that repeatedly steps through the list, compares adjacent elements and swaps them if they are in the wrong order. The pass through the list is repeated until the list is sorted. The algorithm, which is a comparison sort, is named for the way smaller or larger elements "bubble"     to the top of the list. 
   * 遍歷所有的數據，每次對相鄰元素進行兩兩比較，如果順序和預先規定的順序不一樣，就進行位置交換。這樣會將最大或最小的數據浮到頂層，之後在重複操作，直到所有的數據有序。
   * ![avatar](https://pic3.zhimg.com/v2-b7d216a5b292cf3a5412bbc7fbb56a9e_b.webp)