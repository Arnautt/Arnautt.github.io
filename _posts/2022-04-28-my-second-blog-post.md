---
title: 'Jupyter notebooks on server'
date: 2022-04-28
permalink: /posts/2022/04/blog-post-jupyter-notebook/
tags:
  - Jupyter notebook
  - SSH
---

To run a Jupyter Notebook from a server, on local machine, start by connecting with ssh


```bash
ssh user@servername
```


Then on the server, run a Jupyter Notebook without web browser and by changing port number


```bash
user@servername $ jupyter notebook --no-browser --port=8887
```

Finally, on local machine run an SSH tunnel by running 


```bash
ssh -N -L localhost:8888:localhost:8887 user@servername
```

*Done !* You can now have access to the notebook located on the server, on localhost:8888.
