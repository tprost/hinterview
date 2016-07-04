+++
date = "2016-06-18T13:34:39-04:00"
title = "Square Matrix Multiplication"
+++

You can multiply two square matrices using a "brute-force" method. This is the intuitive way of doing it.

```
n = A.rows
let C be a new `n * n` matrix
for i = 1 to n
  for j = 1 to n
    cij = 0
    for k = 1 to n
      cij = cij  + aik * bkj
return C
```

The running time is Θ(n^3).

You can use divide and conquer to do square matrix multiplication, and it takes Θ(n^3) as well.


## Strassen's Method

Strassen's method is bloody complicated, but basically it manages to remove one of the recursive matrix multiplications, which makes it more efficient.
