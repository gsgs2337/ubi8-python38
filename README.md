# ubi8-python38-latest


## build

```
$ docker build ./ -t python38
$ docker save python38 > ubi8-python38.tar
$ split -b 50M -d ubi8-python38.tar ubi8-python38.tar_ 
```

## load

```
$ cat ubi8-python38.tar_* > ubi8-python38.tar
$ docker load < ubi8-python38.tar
```

