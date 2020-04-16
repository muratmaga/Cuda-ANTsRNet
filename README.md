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

to push changes to the docker hub 
```
docker login --username=mmaga
docker images #to obtain the imageID of the updated container
docker tag e7d0f21f8714 mmaga/cuda-antsrnet:latest  ## create a new tag with the remote repository username/repo
docker push mmaga/cuda-antsrnet:latest
```




