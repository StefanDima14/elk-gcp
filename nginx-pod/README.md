# NGINX Pod Deployment

This project contains a Kubernetes manifest for deploying an NGINX pod.

## Prerequisites

- A Kubernetes cluster up and running.
- `kubectl` command-line tool installed and configured to communicate with your cluster.

## Applying the Manifest

To create the NGINX pod, apply the manifest using the following command:

```
kubectl apply -f manifests/nginx-pod.yaml
```

## Accessing the NGINX Pod

Once the pod is running, you can access it by port forwarding:

```
kubectl port-forward pod/<nginx-pod-name> 8080:80
```

Replace `<nginx-pod-name>` with the actual name of your NGINX pod. You can then access NGINX at `http://localhost:8080`.

## Cleanup

To delete the NGINX pod, run:

```
kubectl delete -f manifests/nginx-pod.yaml
```