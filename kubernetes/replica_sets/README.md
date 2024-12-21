# Commands

**Create a ReplicaSet from a YAML manifest**:

```bash
kubectl apply -f <file.yaml>
```

**List ReplicaSets**:

```bash
kubectl get replicasets
kubectl get replicasets -o wide
```

**List ReplicaSets in a specific Namespace**:

```bash
kubectl get replicasets -n <namespace>
```

**Describe a ReplicaSet**:

```bash
kubectl describe replicaset <replicaset-name>
```

**View the YAML of a ReplicaSet**:

```bash
kubectl get replicaset <replicaset-name> -o yaml
```

**Scale a ReplicaSet**:

```bash
kubectl scale replicaset <replicaset-number> --replicas=<number>
```

**Delete a ReplicaSet**:

```bash
kubectl delete replicaset <replicaset-name>
```
