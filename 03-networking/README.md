# 03 - Networking in Kubernetes

This folder contains hands-on examples of different networking concepts in Kubernetes, including Services, Ingress, and Network Policies.

---

## Files

### 1. `clusterip-service.yaml`
- **Purpose:** Demonstrates a `ClusterIP` Service.
- **Description:** 
  - Exposes the application on an internal IP within the cluster.
  - Accessible only from other pods within the cluster.
- **Use Case:** Internal communication between pods, not exposed to external traffic.

---

### 2. `nodeport-service.yaml`
- **Purpose:** Demonstrates a `NodePort` Service.
- **Description:** 
  - Exposes the application on a static port on each node.
  - Can be accessed externally using `NodeIP:NodePort`.
- **Use Case:** Quick external access without using an Ingress.

---

### 3. `ingress.yaml`
- **Purpose:** Demonstrates an `Ingress` resource.
- **Description:** 
  - Provides HTTP/S routing to services inside the cluster.
  - Requires an Ingress Controller (e.g., NGINX, Traefik) to function.
- **Use Case:** Managing external access, host-based routing, SSL termination.

---

### 4. `network-policy.yaml`
- **Purpose:** Demonstrates a `NetworkPolicy`.
- **Description:** 
  - Defines allowed traffic to/from pods.
  - Used to secure communication within the cluster.
- **Use Case:** Restrict traffic to only specific pods or namespaces.

---

## How to Apply

```bash
# Apply ClusterIP Service
kubectl apply -f clusterip-service.yaml

# Apply NodePort Service
kubectl apply -f nodeport-service.yaml

# Apply Ingress
kubectl apply -f ingress.yaml

# Apply Network Policy
kubectl apply -f network-policy.yaml
