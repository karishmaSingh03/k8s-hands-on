# 01-core-concepts

This folder contains basic Kubernetes objects: **Namespace** and **Pod**.

## Files

1. **namespace.yaml**
   - Creates a namespace `dev`.
   - Helps isolate resources in a cluster.
   - Useful for separating environments like dev/test/prod.

2. **pod.yaml**
   - Creates a pod `nginx-pod` in `dev` namespace.
   - Runs a single nginx container.
   - Labels allow grouping and selection by other resources.

## Kubectl Commands

```bash
kubectl apply -f namespace.yaml
kubectl get namespaces

kubectl apply -f pod.yaml
kubectl get pods -n dev
kubectl describe pod nginx-pod -n dev
kubectl logs nginx-pod -n dev
