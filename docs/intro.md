---
title: Getting Started with KAPP
---
  
# What is KAPP

KAPP is an intuitive workflow for deploying, managing, and querying applications on kubernetes.

# Why KAPP

Kuberenetes is a powerful and flexible tool for managing microservices. However, it comes with a lot of complexity, and requires high effort to even setup the simplest real world application. As applications scales up, this complexes grows exponentially. 

KAPP tries to mitigate this complexity by make things more intuitive and managable across three facets:

1. Provide intuitive inteface for common operations
2. Introduce high level abstractions(i.e Application, Config) that map to lower level Kubernetes resource types at the [resource definition]() level. This drastically simplifies the amount of boilerplate configuration for many types of popular usecases.
3. Preconfigured Extensions - k8s comes with a vibrant ecosystem. But to even get advanced features, one would have to install and configure multiple extensions. Microservice Applications created by KAPP just works, and get immediate access to powerful features such as Grayscale deployment, autoscaling, external access out of the box. See [Plugins]() for more details.

![KAPP Interface][interface]

# How KAPP Works

 Kapp make some wraps on top of k8s. This is done through the k8s cool feature [Custom Resource Definition](https://kubernetes.io/docs/tasks/access-kubernetes-api/custom-resources/custom-resource-definitions/). We defined some new models which will parse into k8s original ones by Kapp controller.


Its easier to see how this works together by going through an example:

[interface]: /img/intro-ux.png