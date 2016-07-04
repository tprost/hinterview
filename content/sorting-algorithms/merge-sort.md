+++
date = "2016-06-18T13:34:39-04:00"
title = "Merge Sort"
+++

Merge sort uses a **divide and conquer** approach.

## Divide and Conquer Approach

### Divide
Divide the `n-element` sequence to be sorted into two subsequences of `n = 2` elements each.

### Conquer
Sort the two subsequences recursively using merge sort.

### Combine
Merge the two sorted subsequences to produce the sorted answer.

## The Merge Algorithm

### Pseudocode

The key operation of the merge sort algorithm is the merging of two sorted sequences in the “combine” step. We merge by calling an auxiliary procedure MERGE(A, p, q, r), where A is an array and p, q, and r are indices into the array such that p  q<r. The procedure assumes that the subarrays AŒp : : q and AŒq C 1::r are in sorted order. It merges them to form a single sorted subarray that replaces the current subarray AŒp : : r.

```
n1 = q - p + 1
n2 = r - q
let L[1 .. n1 + 1] and R[1 .. n2 + 1] be new arrays
for i = 1 to n1
  L[i] = A[p + i - 1]
for j = 1 to n2
  R[j] = A[q + j]
L[n1 + 1] = infinite
R[n2 + 1] = infinite
i = 1
j = 1
for k = p to r
  if L[i] <= R[j]
    A[k] = L[i]
    i = i + 1
  else A[k] = R[j]
    j = j + 1
```

## The Merge-Sort Algorithm

```
if p < r
  q = floor of (p + r)/2
    merge-sort(A, p, q)
    merge-sort(A, q + 1, r)
    merge(A, p, q, r)
```

## Analysis

The **divide** step just computers the middle of the subarray, which takes constant time. So the divide step takes O(1).

In the **conquer** step, we recursively solve two subproblems, each of size `n/2`, which contributes `2T(n/2)` to the running time.

For the **combine** step, the running time is O(n), the cost of the merge operation.

```
T(n) = O(1)             if n = 1
T(n) = 2T(n/2) + O(n)   if n > 1
```
