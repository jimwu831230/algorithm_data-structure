# Algorithm & Data Structure

## LeetCode

* [Queue & Stack](https://leetcode.com/explore/learn/card/queue-stack/)
  * [circular queue](LeetCode/QueueStack/circularQueue.cpp)

## Links

* [Mastering Markdown · GitHub Guides](https://guides.github.com/features/mastering-markdown/)
  * [Markdown Cheatsheet 中文版](https://gist.github.com/billy3321/1001749662c370887c63bb30f26c9e6e)

## Sorting Algorithm 排序算法
* 
|        排序算法         | 平均複雜度 |   最壞情況   | 空間複雜度 | 排序方式  |
| :---------------------: | :--------: | :----------: | :--------: | :-------: |
|  冒泡排序 Bubble sort   |  $O(n^2)$  |   $O(n^2)$   |   $O(1)$   | In-place  |
| 選擇排序 Selection sort |  $O(n^2)$  |   $O(n^2)$   |   $O(1)$   | In-place  |
| 插入排序 Insertion sort |  $O(n^2)$  |   $O(n^2)$   |   $O(1)$   | In-place  |
|   希爾排序 Shell sort   | $O(nlogn)$ | $O(nlog^2n)$ |   $O(1)$   | In-place  |
|   歸併排序 Merge sort   | $O(nlogn)$ |  $O(nlogn)$  |   $O(n)$   | Out-place |
|   快速排序 quick sort   | $(nlogn)$  |   $O(n^2)$   | $O(logn)$  | In-place  |
|    推排序 Heap sort     | $O(nlogn)$ |  $O(nlogn)$  |   $O(1)$   | In-place  |
| 計數排序 Counting sort  |  $O(n+k)$  |   $O(n+k)$   |   $O(k)$   | Out-place |
|   桶排序 Bucket sort    |  $O(n+k)$  |   $O(n^2)$   |  $O(n+k)$  | Out-place |
|   基數排序 radix sort   |  $O(n+k)$  |   $O(nxk)$   |  $O(n+k)$  | Out-place |
 
   * n: 代表數據規模及數據量大小
   * k: 桶的個數
   * In-place: 不佔用額外內存，只佔用常數內存
   * Out-place: 佔用額外內存

* Bubble sort 冒泡排序法
 * Bubble sort is a simple sorting algorithm that repeatedly steps through the list, compares adjacent elements and swaps them if they are in the wrong order. The pass through the list is repeated until the list is sorted. The algorithm, which is a comparison sort, is named for the way smaller or larger elements "bubble"     to the top of the list. 
 * 遍歷所有的數據，每次對相鄰元素進行兩兩比較，如果順序和預先規定的順序不一樣，就進行位置交換。這樣會將最大或最小的數據浮到頂層，之後在重複操作，直到所有的數據有序。
 * ![avatar](https://pic3.zhimg.com/v2-b7d216a5b292cf3a5412bbc7fbb56a9e_b.webp)
  
* Selection sort 選擇排序法
 * Initially, the sorted sublist is empty and the unsorted sublist is the entire input list. The algorithm proceeds by finding the smallest (or largest, depending on sorting order) element in the unsorted sublist, exchanging (swapping) it with the leftmost unsorted element (putting it in sorted order), and moving the sublist boundaries one element to the right.  
 * 先在數據中找出最大或最小的元素，放到序列的起始，再從剩下的數據中尋找最大或最小的元素，依次排到序列中，直到所有數據樣本排完。
 * ![avatar](https://pic1.zhimg.com/v2-44be35da53ae9ee564ce444542a43d10_b.webp)

* Insertion sort 插入排序法
 * Suppose there exists a function called Insert designed to insert a value into a sorted sequence at the beginning of an array. It operates by beginning at the end of the sequence and shifting each element one place to the right until a suitable position is found for the new element. The function has the side effect of overwriting the value stored immediately after the sorted sequence in the array.
 * 先將待排序列的第一個元素當作有序序列，把第二個元素到最後一個元素當成是未排序序列。從頭到尾依次掃描未排序序列，將掃描到的每個元素插入有序序列的適當位置。 （如果待插入的元素與有序序列中的某個元素相等，則將待插入元素插入到相等元素的後面。）
 * ![avatar](https://pic1.zhimg.com/v2-be81c151f38d8923fe1ede31ac530ac4_b.webp)

* Shell sort 希爾排序法
 * The method starts by sorting pairs of elements far apart from each other, then progressively reducing the gap between elements to be compared. Starting with far apart elements, it can move some out-of-place elements into position faster than a simple nearest neighbor exchange. 
 * 基本思路是先將整個數據序列分割成若干子序列分別進行直接插入排序，待整個序列中的記錄基本有序時，再對全部數據進行依次直接插入排序。
 * 選擇一個增量序列 t1，t2，……，tk，其中 ti > tj, tk = 1；
 * 按增量序列個數 k，對序列進行 k 趟排序；
 * 每趟排序，根據對應的增量 ti，將待排序列分割成若干長度為 m 的子序列，分別對各子表進行直接插入排序。僅增量因子為 1 時，整個序列作為一個表來處理，表長度即為整個序列的長度。
 * ![avatar](https://mmbiz.qpic.cn/mmbiz_gif/D67peceibeISwc3aGibUlvZ0XqVnbWtBRiadtZekLQySMDdNsZTx6jyaO6spIkjPFjwqfdhd2XfRUnic1PjV1yRxrw/640?wx_fmt=gif&tp=webp&wxfrom=5&wx_lazy=1)
   
* Merge sort 歸併排序法
 * Divide the unsorted list into n sublists, each containing one element (a list of one element is considered sorted). Repeatedly merge sublists to produce new sorted sublists until there is only one sublist remaining. This will be the sorted list.
 * 申請空間，使其大小為兩個已經排序序列之和，該空間用來存放合併後的序列；
 * 設定兩個指針，最初位置分別為兩個已經排序序列的起始位置；
 * 比較兩個指針所指向的元素，選擇相對小的元素放入到合併空間，並移動指針到下一位置；
 * 重複步驟 3 直到某一指針達到序列尾；將另一序列剩下的所有元素直接複製到合併序列尾。
 * ![avatar](https://upload.wikimedia.org/wikipedia/commons/c/cc/Merge-sort-example-300px.gif)

* Quick sort 快速排序法
 * Pick an element, called a pivot, from the array. 
 * Partitioning: reorder the array so that all elements with values less than the pivot come before the pivot, while all elements with values greater than the pivot come after it (equal values can go either way). After this partitioning, the pivot is in its final position. This is called the partition operation. 
 * Recursively apply the above steps to the sub-array of elements with smaller values and separately to the sub-array of elements with greater values.
 * 首先從數列中挑出一個元素，並將這個元素稱為「基準」，英文pivot。重新排序數列，所有比基準值小的元素擺放在基準前面，所有比基準值大的元素擺在基准後面（相同的數可以到任何一邊）。在這個分區結束之後，該基準就處於數列的中間位置。這個稱為分區（partition）操作。之後，在子序列中繼續重複這個方法，直到最後整個數據序列排序完成
 * ![avatar](https://mmbiz.qpic.cn/mmbiz_gif/D67peceibeISwc3aGibUlvZ0XqVnbWtBRiaAY3VU8iaziaYcxAasTdrIu69BOVPYtfvqdvicmlJDS94cG2tjwZhVkdHA/640?wx_fmt=gif&tp=webp&wxfrom=5&wx_lazy=1)
  
* Heap sort 堆排序法
 * it divides its input into a sorted and an unsorted region, and it iteratively shrinks the unsorted region by extracting the largest element and moving that to the sorted region. 
 * 創建一個堆 H[0……n-1]；
 * 把堆首（最大值）和堆尾互換；
 * 把堆的尺寸縮小 1，並調用 shift_down(0)，目的是把新的數組頂端數據調整到相應位置；
 * 重複步驟 2，直到堆的尺寸為 1。
 * ![avatar](https://mmbiz.qpic.cn/mmbiz_gif/D67peceibeISwc3aGibUlvZ0XqVnbWtBRian1jgiaGZE9k1xZTp9B1icHia0jIXiba3ibgnIBibdfSN4I5US4WtrQJQMiakw/640?wx_fmt=gif&tp=webp&wxfrom=5&wx_lazy=1) 

* Counting sort 計數排序法
 * 花O(n)的時間掃描一下整個序列 A，獲取最小值 min 和最大值 max
 * 開闢一塊新的空間創建新的數組 B，長度為 ( max - min + 1)
 * 數組 B 中 index 的元素記錄的值是 A 中某元素出現的次數
 * 最後輸出目標整數序列，具體的邏輯是遍歷數組 B，輸出相應元素以及對應的個數
 * ![avatar](https://pic1.zhimg.com/v2-827d96b8ca3682e8775f4916f22b45ac_b.webp)

* Bucket sort 桶排序法
 * 將數組劃分到一定數量的有序的桶裡，然後再對每個桶中的數據進行排序，最後再將各個桶裡的數據有序的合併到一起。
 * ![avatar](https://mmbiz.qpic.cn/mmbiz_gif/D67peceibeISwc3aGibUlvZ0XqVnbWtBRia0umOurgFRv8ESYzcK6bXknufLgJGLaiaTrDTXUk09R6ia2DhbCPAJx0A/640?wx_fmt=gif&tp=webp&wxfrom=5&wx_lazy=1)

* Radix sort 基數排序法
 * 將所有待比較數值（正整數）統一為同樣的數位長度，數位較短的數前面補零
 * 從最低位開始，依次進行一次排序
 * 從最低位排序一直到最高位排序完成以後, 數列就變成一個有序序列
 * ![avatar](https://mmbiz.qpic.cn/mmbiz_gif/D67peceibeISwc3aGibUlvZ0XqVnbWtBRial8LfeK5f941BmtmZcVlP0my2qgBXq6wEZ0PTDrcPqN3ntt7ibPrUxrg/640?wx_fmt=gif&tp=webp&wxfrom=5&wx_lazy=1)


     
