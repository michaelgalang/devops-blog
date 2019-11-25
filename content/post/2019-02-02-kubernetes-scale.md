---
title: Scaling My Kubernetes Deployment
date: 2019-02-02
tags: ["kubernetes", "code"]
---

Scaling my Kubernetes deployment

<!--more-->

```sh
    $ kubectl scale deployments/kubernetes-bootcamp --replicas=4
```

Now, check whether it is scaled up:
```sh
    $ kubectl get deployments
    NAME               DESIRED  CURRENT   UP-TO-DATE    AVAILABLE  AGE
    kubernets-bootcamp 4        4         4             4          26s
    
    $ kubectl get pods -o wide
    NAME                        READY       STATUS      RESTART     AGE     IP              NODE
    kubernets-bootcamp-12345    1/1         Running     0           3s      172.18.0.7      minikube
    kubernets-bootcamp-23456    1/1         Running     0           3s      172.18.0.4      minikube
    kubernets-bootcamp-asc34    1/1         Running     0           3s      172.18.0.5      minikube
    kubernets-bootcamp-456tf    1/1         Running     0           20s     172.18.0.8      minikube
```

