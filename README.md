# docker-swarm-bootstrap

based on https://docs.docker.com/swarm/install-manual

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


### swarm

#### set up primary swarm manager
```
$ ./gradlew swarmManagerPrimarySetup
```

#### set up replica swarm managers
```
$ ./gradlew swarmManagerReplicaSetup
```

### set up swarm agents
```
$ ./gradlew swarmAgentsSetup
```
