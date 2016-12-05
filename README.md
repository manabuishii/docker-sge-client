# docker-sge-client
Sun Grid Engine Client in Docker

# hub.docker.com

* [manabuishii/docker-sge-client on hub.docker.com](https://hub.docker.com/r/manabuishii/docker-sge-client/)

## pull

```
docker pull manabuishii/docker-sge-client:0.1.0
```

# HOW TO RUN

```
docker run -e RUNUSER_USERNAME=manabu \
          -e RUNUSER_UID=2000 \
          -e RUNUSER_GID=2000 \
          -e RUNUSER_HOME=$HOME \
          -v $HOME:$HOME:ro  \
          --rm \
          --net=host \
          -ti \
          -v $PWD/act_qmaster:/var/lib/gridengine/default/common/act_qmaster  \
          --name sgetest manabuishii/docker-sge-client:0.1.0 /bin/bash
```

# HOW TO SUBMIT

```
echo "hostname; date" | qsub
```

or output file create on exec host /tmp

```
echo "hostname; date" | qsub -o /tmp/myjob1.txt
```



# NOTE

- --net=host means your docker container connect with docker host name
- submit user name is important.
