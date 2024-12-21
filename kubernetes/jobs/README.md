# Commands

**Create a Job from a YAML Manifest**:

```bash
kubectl apply -f <file.yaml>
```

**List All Jobs**:

```bash
kubectl get jobs
```

**List Jobs in a Specific Namespace**:

```bash
kubectl get jobs -n <namespace>
```

**Describe a Job**:

```bash
kubectl describe job <job-name>
```

**View the YAML of a Job**:

```bash
kubectl get job <job-name> -o yaml
```

**Delete a Job**:

```bash
kubectl delete job <job-name>
```

**Delete All Jobs in a Namespace**:

```bash
kubectl delete jobs --all -n <namespace>
```

**Force Delete a Job and Its Pods**:

```bash
kubectl delete job <job-name> --cascade=foreground
```
