---
title: gsw-xarray
description: "gsw-xarray: wrap gsw for xarray and pint-xarray"
permalink: /gsw-xarray
layout: default
---

# Simple usage
## Installation

```bash
pip install gsw-xarray
# or
conda install -c conda-forge gsw-xarray
```

## Usage

For most usage, you can use it as a drop in replacement for gsw:

```python
import gsw_xarray as gsw

# Use it as you used gsw, e.g. gsw.sigma0(SA=ds.SA, CT=ds.CT)
```

Use with pint quantities:

```python
import gsw_xarray as gsw
import pint
ureg = pint.UnitRegistry()
SA = ureg.Quantity(35, ureg("g/kg"))
CT = ureg.Quantity(10, ureg.degC)
sigma0 = gsw.sigma0(SA=SA, CT=CT)
print(sigma0)
```

Outputs

```
26.824644457868317 kilogram / meter ** 3
```
