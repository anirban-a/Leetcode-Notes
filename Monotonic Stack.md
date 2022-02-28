# Monotonic stack.

## Introduction

Consider a stack `S` containing the elements `[s1, s2, s3, s4,..sn]`. The stack `S` is considered to be monotonic if for all `i` where `1 <i<=n`, there exists `j` where `0<=j<i`, `S[j]>=S[i]` **or** `S[j]<=S[i]`. In simple words, a monotonic stack is containing elements which are either in non-decreasing order or in non-increasing order.

## Use-cases

A monotonically increasing stack can be used where you are given a list of items (such as `ints`) and you are looking at `i-th` element from that list and you want to refer back to a set of elements from that collection that have been either less or equal to the current element. In case of strictly monotonically increasing stack, all the elements in the stack preceding the current element from the list to be added is definitely going to be less.

### Example

Given the list `A` as follows:

```
A = [2, 3, 4, 1, 5]
```
A strictly monotonically increasing stack `S` will look like the following for indices 0 through 2 of the list `A`:

```
S = [2, 3, 4]
```

When we encounter the element at index 3, `A[3]` is `1` which is less than the top of the stack which is `4`. So we pop it. And we keep doing this for as long as the top of the stack is either less than or equal to my current element. Which means the `S` will now look like:

```
S = [1]
```

Continuing this process our final state of `S` will be:

```
S = [1, 5]
```
