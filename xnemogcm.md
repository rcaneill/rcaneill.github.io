---
title: xnemogcm
description: "xnemogcm: open nemo data"
permalink: /xnemogcm
layout: default
---

# Simple usage
## Installation

```bash
pip install xnemogcm
# or
conda install -c conda-forge xnemogcm
```

## Open nemo data

```python
from pathlib import Path
from xnemogcm import open_nemo_and_domain_cfg

ds = open_nemo_and_domain_cfg(
    nemo_files=['/path/to/output/file'],
    domcfg_files=['/path/to/domain_cfg/mesh_mask/file']
)

# Interface with xgcm
from xnemogcm import get_metrics
import xgcm
grid = xgcm.Grid(ds, metrics=get_metrics(ds), periodic=False)
```
