# Jupyter Images

> See <https://github.com/kubeflow/kubeflow/tree/master/components/example-notebook-servers> for more information.

This repository contains the Dockerfiles for the Jupyter images that can be used in kubeflow.

There are currently 6 different images:

- basic [JupyterLab](https://github.com/jupyterlab/jupyterlab) image
- JupyterLab image with PyTorch
- JupyterLab image with DeepSpeed
- basic [code-server](https://github.com/coder/code-server) image
- code-server image with PyTorch
- code-server image with DeepSpeed

The basic idea is that we provide images with some complicated dependencies pre-installed, so that users can get started with their work without having to worry about the installation process. These complicated dependencies includes:

- PyTorch: not too difficult to install, but it's a large package and it takes a long time.
- DeepSpeed: requires compile from source to enable all features, which has complicated dependency matrix.

## Special Image Dependencies

image | tag | PyTorch | cuda | cudnn
---|---|---|---|---
zjuici/jupyter | 0.5.0-pytorch | 2.0.1 | 11.7 | cudnn8
zjuici/codeserver | 0.5.0-pytorch | 2.0.1 | 11.7 | cudnn8

image | tag | DeepSpeed | PyTorch | cuda | cudnn
---|---|---|---|---|---
zjuici/jupyter | 0.5.0-deepspeed | v0.9.5 | 1.13.1 | 11.6 | cudnn8
zjuici/codeserver | 0.5.0-deepspeed | v0.9.5 | 1.13.1 | 11.6 | cudnn8
