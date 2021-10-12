# Eclipse
> Implementing Paletta et al. in Pytorch


Most of the codebase comes from [Fiery](https://github.com/wayveai/fiery)

![Image](nbs/images/eclipse_diagram.png)

## Install

```bash
pip install eclipse_pytorch
```

## How to use

```python
import torch

from eclipse_pytorch.model import Eclipse
```

```python
eclipse = Eclipse(horizon=5)
```

let's simulte some input images:

```python
images = [torch.rand(2, 3, 128, 128) for _ in range(4)]
```

```python
preds = eclipse(images)
```

you get a dict with forecasted masks and irradiances:

```python
len(preds['masks']), preds['masks'][0].shape, preds['irradiance'][0].shape
```




    (6, torch.Size([2, 3, 128, 128]), torch.Size([2, 1]))


