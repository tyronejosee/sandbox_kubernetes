# Commands

**Create a ConfigMap from a file**:

```bash
kubectl create configmap <configmap-name> --from-file=<file-path>
```

**Create a ConfigMap from multiple files**:

```bash
kubectl create configmap <configmap-name> --from-file=<file-path> --from-file=<file-path>
```

**Create a ConfigMap from key-value pairs**:

```bash
kubectl create configmap <configmap-name> --from-literal=<key>=<value>
```

**Apply a ConfigMap from a YAML manifest**:

```bash
kubectl apply -f <file.yaml>
```

**List ConfigMaps**:

```bash
kubectl get configmaps
```

**List ConfigMaps for a specific Namespace**:

```bash
kubectl get configmaps -n <namespace>
```

**Describe a ConfigMap**:

```bash
kubectl describe configmap <configmap-name>
```

**View the data of a ConfigMap**:

```bash
kubectl get configmap <configmap-name> -o yaml
```

**Delete a ConfigMap**:

```bash
kubectl delete configmap <configmap-name>
```

**Edit an existing ConfigMap**:

```bash
kubectl edit configmap <configmap-name>
```

**Export an existing ConfigMap**:

```bash
kubectl get configmap <configmap-name> -o yaml > <file.yaml>
```
