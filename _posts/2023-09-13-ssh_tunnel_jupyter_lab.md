---
layout: post
title:  "Access a remote jupyter lab server with ssh tunneling"
date:   2023-09-13
categories: tools
description_long: "I am usually running analyses on a remote server, which I thought was not easily compatible with using jupyter lab."
---

{{ page.description_long }}

The truth is: I was wrong. It is very easy to launch a jupyter lab server in
a remote computer (e.g. via a ssh connection), and access it from a laptop in a
browser with a GUI. I am sharing the solution here, mainly because I want to remember
it, I hope it may also help you.

So here are the steps:
1. Login via ssh to the remote server and launch jupyter lab
2. In the local computer, open a terminal and start a ssh tunnel:
```
ssh -N -L 8888:localhost:8888 user@remotehost
```
The `8888` port is the common jupyter
lab port. If your jupyter lab is using another port, change it accordingly in the command.
3. Open `localhost:8888` in your browser, and voila!


> **Note:**
jupyter lab may start with a token, in this case paste `localhost:8888/?token=THETOKEN`
in your browser (the token is given when jupyter lab starts).


> **Note:**
I am using [snakemake](https://snakemake.readthedocs.io/) and the great possibility to
use jupyter notebooks in it. When I use the `--edit-notebook` option on the remote server,
I then simply need to use the ssh tunnel to edit my notebook in my browser. Very convenient!
