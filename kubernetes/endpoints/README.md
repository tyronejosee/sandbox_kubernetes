# Commands

**List Endpoints**:

```bash
kubectl get endpoints
```

**List Endpoints in a specific Namespace**:

```bash
kubectl get endpoints -n <namespace>
```

**List the details of a specific endpoint**:

```bash
kubectl get endpoints <endpoints-name>
```

**Describe an Endpoint**:

```bash
kubectl describe endpoints <endpoints-name>
```

**View Endpoints in YAML format**:

```bash
kubectl get endpoints <endpoints-name> -o yaml
```

**View Endpoints in JSON format**:

```bash
kubectl get endpoints <endpoints-name> -o json
```

**Delete an Endpoint**:

```bash
kubectl delete endpoints <endpoints-name>
```

**View Endpoints with a label selector**:

```bash
kubectl get endpoints -l <label-selector>
```
