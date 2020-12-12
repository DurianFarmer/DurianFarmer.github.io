---
layout: post
title: Selecting GPU among Multi GPUs
categories:
  - GPU
tags:
  - GPU
  - CUDA
  - torch
---

### This code is useful when you want to select a GPU nobody else is using

```python
import torch

GPU_NUM = 3 # select a gpu number 
device = torch.device('cuda' if torch.cuda.is_available() else 'cpu')
print ('Available devices ', torch.cuda.device_count())
print ('Previous cuda device ', torch.cuda.current_device())
print(torch.cuda.get_device_name(device))

device = torch.device(f'cuda:{GPU_NUM}' if torch.cuda.is_available() else 'cpu')
torch.cuda.set_device(device) # change allocation of current GPU
print ('New cuda device ', torch.cuda.current_device()) # check
torch.backends.cudnn.deterministic = True
```

<!--more-->