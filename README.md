An attempt at making a portable ANTsR docker app, with tensorflow-gpu and CUDA

```
docker build --build-arg IMAGE_NAME=nvidia/cuda -t antsrnet:initial .
```

and run it with 

```
docker run -it --gpus all antsrnet:initial /bin/bash

```
REMINDER: Make changes to virtual environment and them commit locally


