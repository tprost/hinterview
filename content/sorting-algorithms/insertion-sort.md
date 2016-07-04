+++
date = "2016-06-18T13:34:39-04:00"
title = "Insertion Sort"
+++

## Pseudocode

Start at A[2] and work towards the end. Insert each item into the beginning part of the array where appropriate.

```
for j = 2 to A.length
  key = A[j]
  // Insert A[j] into the sorted sequence A[1 .. j - 1]
  i = j - 1
  while i > 0 and A[i] > key
    A[i + 1] = A[i]
    i = i - 1
  A[i + 1] = key
```

## Correctness

We can use *loop invariants* to prove the correctness. We should examine both loops but we are lazy, so let's just examine the outer loop.

### The Loop Invariant

The loop invariant is as follows:

> At the start of each iteration of the outer `for` loop, the subarray `A[1 .. j - 1]` consists of the elements originally in `A[1 .. j - 1]`, but in sorted order.

#### Initialization

The loop invariant holds before the first loop iteration, because the subarray `A[1 .. j - 1]` has only one element and is trivially sorted.

#### Maintenance

The subarray `A[1 .. j]` is in sorted order because of reasons.

#### Termination

When we terminate, `j = n + 1`. Therefore, `A[1 .. n]` is sorted.

