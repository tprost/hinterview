+++
date = "2016-06-18T13:34:39-04:00"
title = "Bubble Sort"
+++

Bubble sort is where you compare some pairs until the shit is sorted.

## Pseudocode

```
for i = 1 to A.length - 1
  for j = A.length downto i + 1
    if A[j] < A[j - 1]
      exchange A[j] with A[j - 1]
```

## Correctness

> At the start of each iteration of the inner `for` loop, A[j] <= A[j + 1 .. A.length].

This is true because:

When `j = A.length`, this is true because there are no elements to compare it to.
When `j = A.length - 1`, this is true because trivially, A[A.length] cannot be less than A[A.length - 1], because if would have been swapped in the previous iteration.
For any `j`, we know that:

A[j + 1] >= A[j]

and if A[j + 1] <= A[j + 2 .. A.length], then A[j] <= A[j + 1 .. A.length]

So inductively, we prove the loop invariant.

When the loop terminates, A[i + 1] <= A[i + 2 .. A.length].

> At the start of each iteration of the outer `for` loop, A[i - 1 + 1] <= A[i - 1 + 2 .. A.length], so A[i] <= A[i + 1 .. A.length].

Blah dee blah.

