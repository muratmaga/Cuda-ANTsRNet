An attempt at making a portable ANTsR docker app, with tensorflow-gpu and CUDA

```
docker build --build-arg IMAGE_NAME=nvidia/cuda -t antsrnet:initial .
```

and run it with 

```
docker run -it --gpus all antsrnet:initial /bin/bash

```
REMINDER: Make changes to virtual environment and commit them locally

```
docker ps -a #look for the CONTAINER_ID and then 
docker commit f1e986f2dcf1 antsrnet:latest
````

remove the existing docker and then re-run to make sure changes are incorpored

```
docker rm f1e986f2dcf1
docker run -it --gpus all antsrnet:latest /bin/bash
```

