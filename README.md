Jupyter Lab Docker image with eWaterCycle dependencies installed.

[![](https://images.microbadger.com/badges/version/ewatercycle/jupyterlab-experiment-builder.svg)](https://hub.docker.com/r/ewatercycle/jupyterlab-experiment-builder/)

# Usage

To start JupyterLab on http://localhost:8888 use
```bash
docker run -it --rm -p 8888:8888 ewatercycle/jupyterlab-experiment-builder
```

To persist notebooks in current directory use
```bash
docker run -e NB_UID=$(id -u) -e NB_GID=$(id -g) -v $PWD:/home/jovyan -it --rm -p 8888:8888 ewatercycle/jupyterlab-experiment-builder
```

# Build

```bash
docker build -t ewatercycle/jupyterlab-experiment-builder .
```

Based on https://github.com/jupyter/docker-stacks/tree/master/scipy-notebook
