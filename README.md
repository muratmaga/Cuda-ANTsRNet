An attempt at making a portable ANTsR docker app, with tensorflow-gpu and CUDA

```
docker build --build-arg IMAGE_NAME=nvidia/cuda .
```

Users should run into bash directly

```
docker run -it --gpus all --rm antsr:latest /bin/bash
```
