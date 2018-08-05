# Run the Jupyter notebook

[![GuardRails badge](https://badges.production.guardrails.io/shtakai/chainer-handson.svg)](https://www.guardrails.io)

You can download and run the notebooks on your Jupyter-enabled machine.

## Tested environment

- Ubuntu 14.04 LTS
- NVIDIA GPU (recommended GTX 970 or higher)
- CUDA 7.5 (installed under /usr/local/cuda)
  - cuDNN v4 (optional)
- Python 2.7 / 3.4
- Chainer v1.20.0.1
  - All version after v1.5.0 should work
- Additional python packages
  - pyparsing == '2.1.10'
  - pydot == '1.2.3'
  - jupyter
  - matplotlib

## Set up

Copy .ipynb files, data.py, and image directory into a jupyter-managed directory.

## Start 

```
$ jupyter notebook
```


# Build a Chainer & Jupyter environment from scratch on 

This repository also provide helper scripts to install CUDA, Chainer, and Jupyter on Ubuntu 14.04.

## Install CUDA 7.5 and CUDA toolkit

CUDA libraries will be installed into `/usr/local/cuda/`.

```
$ ./install-cuda.sh
```
Reboot is needed before proceeding. You can also install cuDNN by yourself at this point.

## Install Chainer

Python packages will be installed under `$HOME/.local/` with `pip install --user`

```
$ ./install-chainer.sh
```

## Install Jupyter and visualization packages

```
$ ./install-jupyter.sh
```

## Run the Jupyter notebook with preset config

Make sure that the environmental variables are loaded.

```
$ source ~/.bash_profile
$ jupyter notebook
```

The access URL is `https://<ip address>:8888/`. The password is "chainer".
