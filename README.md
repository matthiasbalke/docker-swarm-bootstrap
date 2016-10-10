# docker-swarm-bootstrap

## vagrant

### create dev vm's
```
$ vagrant up
```

### docker

#### install on all defined hosts
```
$ ./gradlew dockerInstall
```

#### check installed version
```
$ ./gradlew dockerCheck
```


### consul

#### set up service discovery
```
$ ./gradlew consulStart
```
