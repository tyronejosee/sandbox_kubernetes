# Commands

**Create a StatefulSet from a YAML manifest**:

```bash
kubectl apply -f <file.yaml>
```

**List all StatefulSets**:

```bash
kubectl get statefulsets
```

**List StatefulSets in a specific namespace**:

```bash
kubectl get statefulsets -n <namespace>
```

**Describe a StatefulSet**:

```bash
kubectl describe statefulset <statefulset-name>
```

**View the YAML of a StatefulSet**:

```bash
kubectl get statefulset <statefulset-name> -o yaml
```

**Scale a StatefulSet (modify the number of replicas)**:

```bash
kubectl scale statefulset <statefulset-name> --replicas=<number>
```

**Delete a StatefulSet**:

```bash
kubectl delete statefulset <statefulset-name>
```
