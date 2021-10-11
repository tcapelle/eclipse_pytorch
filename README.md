# Eclipse
> Implementing Paletta et al. in Pytorch


![Image](nbs/images/eclipse_diagram.png)

## Install

`pip install eclipse_pytorch`

## How to use

```python
import torch

from eclipse_pytorch.model import *
```

```python
eclipse = Eclipse()
```

```python
preds = eclipse([torch.rand(2, 3, 256, 256) for _ in range(4)])
```

    states.shape=torch.Size([2, 4, 128, 32, 32])
    present_state.shape=torch.Size([2, 1, 128, 32, 32])
    hidden_state.shape=torch.Size([2, 128, 32, 32])
    future_states.shape=torch.Size([2, 6, 128, 32, 32])

