# flux-get-started

[![CircleCI](https://circleci.com/gh/cnb0/learning-flux-cd.svg?style=svg)](https://circleci.com/gh/cnb0/learning-flux-cd)

step-by-step run-through on how to use Flux and Helm Operator [over
here](https://github.com/fluxcd/flux/blob/master/docs/tutorials/get-started-helm.md).

## Workloads

[podinfo](https://github.com/stefanprodan/podinfo)
* Kubernetes deployment, ClusterIP service and Horizontal Pod Autoscaler
* init container automated image updates (regular expression filter)
* container automated image updates (semantic versioning filter)

## Helm Releases

Mongodb
* Source: Helm repository (stable)
* Kubernetes deployment
* automated image updates (semantic versioning filter)

Redis
* Source: Helm repository (stable)
* Kubernetes stateful set 
* locked automated image updates (semantic versioning filter)

Ghost
* Source: Git repository
* disabled automated image updates (glob filter)
* has external dependency - mariadb (stable)

## Manifests Validation

CircleCI [jobs](./.circleci/config.yml):
* validate Kubernetes manifests with [kubeval](https://github.com/instrumenta/kubeval)
* validate Flux Helm Releases with [hrval](https://github.com/stefanprodan/hrval-action)


