# ubi8-python38-latest


## build

```
$ cat Dockerfile 

FROM registry.access.redhat.com/ubi8/python-38

CMD sleep 300

$ docker build ./ -t python38
$ docker save python38 > ubi8-python38-latest.tar
$ split -b 50M -d ubi8-python38-latest.tar ubi8-python38-latest.tar_ 
```

## load

```
$ docker load < ubi8-python38-latest.tar
```

