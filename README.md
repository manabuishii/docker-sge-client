# docker-sge-client
Sun Gridengine Client in Docker

# HOW TO RUN

```
docker run -e RUNUSER_USERNAME=manabu -e RUNUSER_UID=2000 -e RUNUSER_GID=2000 -e RUNUSER_HOME=$HOME -v $HOME:$HOME:ro  --rm --net=host -ti -v $PWD/act_qmaster:/var/lib/gridengine/default/common/act_qmaster  --name sgetest manabuishii/docker-sge-client:0.1.0 /bin/bash
```

# NOTE

- --net=host means your docker container connect with docker host name
- submit user name is important.

