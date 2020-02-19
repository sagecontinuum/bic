MinIO Setup on Nautilus
=====

[MinIO](https://min.io) is one option for Sage's object storage solution.
 
Introduction
------------

This modified chart starts the MinIO deployment on [Nautilus](https://nautilus.optiputer.net/), a [Kubernetes](http://kubernetes.io) cluster using the [Helm](https://helm.sh) package manager.

Installing the modified chart
--------------------

Install the modified chart using:

```bash
$ helm install sage-minio --set resources.limits.cpu=8,\
    resources.limits.memory=32Gi,resources.requests.memory=8Gi,\
    resources.requests.cpu=4,persistence.size=100Gi,\
    accessKey=myaccesskey,secretKey=mysecretkey stable/minio
```

The command deploys MinIO on the Nautilus cluster where `accessKey` and `secretKey` are provided by the user.

Ingress setup
-------------
The following command exposes the internal HTTP with [Ingress](https://kubernetes.io/docs/concepts/services-networking/ingress/)

```bash
$ kubectl create -f ingress.yaml
```

