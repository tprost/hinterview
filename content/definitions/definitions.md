+++
date = "2016-06-18T13:34:39-04:00"
title = "Algorithms"
+++

<dl>
  <dt>instance of a problem</dt>
  <dd>In general, an *instance of a problem* consists of the input needed to computer a solution to the problem.</dd>
  <dt>correctness</dt>
  <dd>An algorithm is said to be *correct* if, for every input instance, it halts with the correct output.</dd>
  <dt>running time</dt>
  <dd>Time it takes for an algorithm to run.</dd>
  <dt>input size</dt>
  <dd>Size of an instance of a problem.</dd>
  <dt>worst-case running time</dt>
  <dd>The longest running time for <em>any</em> input of size <code>n</code>.</dd>
  <dt>average-case analysis</dt>
  <dd>Sometimes we use probabilistic analysis to calculate the average-case running time, which is the average running time across all possible inputs. Sometimes we assume all inputs are equally likely and sometimes we don't.</dd>

  <dt>divide and conquer</dt>
  <dd>An approach to designing algorithms in which the problem is broken into several subproblems that are similar to the original problem, but smaller in size.</dd>
  
  <dt>recurrence equation</dt>
  <dd>An equation which describes the overall running time on a problem of size <code>n</code> in terms of the running time on smaller inputs.</dd>
</dl>

## Θ-notation

Θ((g(n)) = { f(n) : there exist positive constants c1, c2, and n0 such that 0 <= c1g(n) <= f(n) <= c2g(n) for all n >= n0}

https://en.wikipedia.org/wiki/Big_O_notation#Family_of_Bachmann.E2.80.93Landau_notations

## The master method for solving recurrences

You need a recurrence of the form

T(n) = aT(n/b) + f(n)

where a  1 and b>1 are constants and f .n/ is an asymptotically positive function.

<img src="/definitions/the-master-theorem.png">
