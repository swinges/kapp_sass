---
title: Installation
---

### Compatibility Matrix

kapp is intended to be backward compatible. It is always recommended to use the latest version of kapp with whatever version of Kubernetes you are using. The numbering follows the semantic versioning specification, MAJOR.MINOR.PATCH.

_**TODO** test usability on each version of k8s._

| kapp version | k8s 1.14.x | k8s 1.15.x | k8s 1.16.x | k8s 1.17.x |
| ------------ | ---------- | ---------- | ---------- | ---------- |
| 0.1.0        | ✔          | ✔          | ✔          | ✔          |

### Prerequisite

k8s cluster is required.

kubectl is required, see [here](https://kubernetes.io/docs/tasks/tools/install-kubectl/).

A cluster-admin role is required to install kapp on your cluster. If you are not familiar with k8s RBAC, you can just use the very first user of your cluster.

### Installing

Install via kubectl

```
kubectl apply -f https://xx.com/xx/xx
# TODO: fix the path.
```

Check install status with the following command. If you see **kapp-controller**, **kapp-dashboard** are up and running, which means kapp is already installed successfully on your cluster.

```
kubectl get pods -n kapp-system
```

Access your dashboard

1. start a proxy server on your localhost

```
kubectl proxy
```

2. open dashboard at [http://localhost:8001/api/v1/namespaces/kapp-system/services/https:kapp-dashbaord:/proxy/](http://localhost:8001/api/v1/namespaces/kapp-system/services/https:kapp-dashbaord:/proxy/)

