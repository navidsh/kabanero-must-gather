# Kabanero must-gather

`Kabanero must-gather` is a tool built on top of [OpenShift must-gather](https://github.com/openshift/must-gather) that expands its capabilities to gather information about Kabanero instances.

### Usage
```sh
oc adm must-gather --image=docker.io/navidsh/kabanero-must-gather:latest
```

The command above will create a local directory with a dump of the Kabanero collection state. Note that this command will only get data related to the Kabanero Collection of the OpenShift cluster. _The must-gather scripts are copy of scripts provided in [Kabanero Foundation](https://github.com/kabanero-io/kabanero-foundation)._

In order to get data about other parts of the cluster (not specific to Kabanero) you should run just `oc adm must-gather` (without passing a custom image). Run `oc adm must-gather -h` to see more options.