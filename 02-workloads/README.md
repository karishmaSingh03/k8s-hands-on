# Kubernetes Workloads

This directory covers **Kubernetes workload resources** that define **how applications are deployed, scaled, and managed** in a cluster.

These YAMLs are aligned with:
- **CKA exam objectives**
- **Real-world production workloads**
- **Common DevOps interview questions**

---

##  Workloads Covered

| Resource | Purpose |
|--------|--------|
| Deployment | Stateless applications with rolling updates |
| ReplicaSet | Maintains desired pod replicas |
| StatefulSet | Stateful apps with stable identity |
| DaemonSet | Runs one pod per node |
| Job | One-time batch workloads |

---

## 📄 Files Overview
02-workloads/
├── deployment.yaml # Defines stateless application deployment with rolling updates
├── replicaset.yaml # Ensures a specified number of pod replicas are running
├── statefulset.yaml # Manages stateful applications with stable pod identity
├── daemonset.yaml # Runs a pod on every node in the cluster
└── cronjob.yaml # Schedules recurring batch jobs
