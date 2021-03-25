---
layout: post
title: Numpy Cookbook
categories:
  - numpy
  - cookbook
tags:
  - numpy
  - cookbook
---

<!--more-->

| Code | Memo |
| --- | --- |
| `np.eye(np.max(y) + 1)[y]` | y를 onehot으로 변환. <br> y는 class를 정수로 표현한 vector |
| `idx = np.argpartition(X, k, axis = 1)`  <br> `X[idx[:,:k]]`| 행렬 X의 row별로 가장 **작은** 값을 가지는 원소 k개의 index를 sort하지 않고 리턴 |
| `idx = np.argpartition(X, -k, axis = 1)`  <br> `X[idx[:,-k:]]`| 행렬 X의 row별로 가장 **큰** 값을 가지는 원소 k개의 index를 sort하지 않고 리턴 |
| `X = np.array([1,2,3])` <br> `print(X.reshape(-1,1))` | row vector를 column vector로 |
| `np.bincount(x).argmax()` | the most frequently appearing element in vector *x* (not a matrix or higher tensor) |
| `np.argmax( np.apply_along_axis(np.bincount, 1, Y, None, np.max(Y)+1), axis=1 )` | the most frequently appearing element for matrix or higher tensor *Y* |






 