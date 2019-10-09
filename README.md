# Kabanero must-gather

`Kabanero must-gather` is a tool built on top of [OpenShift must-gather](https://github.com/openshift/must-gather) that expands its capabilities to gather information about Kabanero instances.

### Usage
```sh
oc adm must-gather --image=docker.io/navidsh/kabanero-must-gather:latest
```

**Note:** `must-gather` flag is a new feature added to `oc v4.x`. If you are using an older version of `oc`, you can get a new version of the CLI from [here](https://mirror.openshift.com/pub/openshift-v4/clients/oc/4.2/). You can use `oc v4.x` against `3.11` cluster.

The command above will create a local directory with a dump of the Kabanero collection state. Note that this command will only get data related to the Kabanero Collection of the OpenShift cluster. _The must-gather scripts are copy of scripts provided in [Kabanero Foundation](https://github.com/kabanero-io/kabanero-foundation)._

In order to get data about other parts of the cluster (not specific to Kabanero) you should run just `oc adm must-gather` (without passing a custom image). Run `oc adm must-gather -h` to see more options.
