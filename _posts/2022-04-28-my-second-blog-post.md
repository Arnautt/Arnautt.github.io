---
title: 'Jupyter notebooks on server'
date: 2022-04-28
permalink: /posts/2022/04/blog-post-jupyter-notebook/
tags:
  - Jupyter notebook
  - SSH
---

Test blog post with Python code : 


```bash
ssh remote_username@remote_host
```


Then on the server


```bash
remote_username@remote_host $ jupyter notebook --no-browser --port=8887
```

Finally, on local machine : 


```bash
ssh -N -L localhost:8888:localhost:8887 remote_username@remote_host
```
