# deep-and-machine-learning-playground

docker image + jupyter notebook UI for learning and experimenting with deep and machine learning.

docker image based on <https://github.com/floydhub/dl-docker> - All-in-one Docker image for Deep Learning

docker hub image @ <https://hub.docker.com/r/pfeilbr/deep-and-machine-learning/>

## Running

```sh
docker run -it -p 8888:8888 -p 6006:6006 -v /Users/brianpfeil/projects/deep-and-machine-learning-playground:/root/sharedfolder pfeilbr/deep-and-machine-learning:v2 bash

# this lands you at a bash prompt in the container
# start jupyter
jupyter notebook

# open browser to http://localhost:8888/
```

## To save container changes

for example to save software installs (e.g. apache mxnet was added to image)

```sh
# list images to find commit id
docker ps -a

# commit changes
# docker commit 5b4a6fb7117b pfeilbr/deep-and-machine-learning:TAG
# e.g. 
docker commit 5b4a6fb7117b pfeilbr/deep-and-machine-learning:v2

# push new image to docker hub
# docker push pfeilbr/deep-and-machine-learning:TAG
# e.g.
docker push pfeilbr/deep-and-machine-learning:v2
```
