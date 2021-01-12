# Demo 1

This demo illustrates how to deploy an HTTP application to [AKS](https://docs.microsoft.com/en-us/azure/aks/) -- Azure's hosted Kubernetes service. We've pre-built a web application that displays [XKCD comics](https://xkcd.com/) and pushed it to [Docker Hub](https://hub.docker.com/r/arschles/xkcd).

This deployment is composed of:

- A [`Deployment`](https://kubernetes.io/docs/concepts/workloads/controllers/deployment/) to create and manage the pods that run the HTTP application
- A [`Service`](https://kubernetes.io/docs/concepts/services-networking/service/) that provisions an Azure Load Balancer with a public IP, directs traffic from the load balancer to the cluster, and forwards that traffic to one of the pods in the deployment (traffic will be evenly balanced across each pod)

## Demo Instructions

You need to have a working Kubernetes cluster, and your `kubectl` tool configured to access the cluster. After you've done so, run the below commands:

```shell
kubectl create namespace appinno1
kubectl create -f ./deployment.yaml --namespace appinno1
kubectl create -f ./service.yaml --namespace appinno1
```

If you want to delete the application, simply delete the namespace:


```shell
kubectl delete ns appinno1
```
