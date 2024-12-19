# Commands

## List all Pods in the cluster

```bash
kubectl get pods --all-namespaces
```

## List Pods in a specific namespace

```bash
kubectl get pods -n <namespace>
```

## View details of a specific Pod

```bash
kubectl describe pod <pod-name> -n <namespace>
```

## View logs of a Pod

```bash
kubectl logs <pod-name> -n <namespace>
```

## View logs of a specific container within a Pod

```bash
kubectl logs <pod-name> -n <namespace> -c <container-name>
```

### Execute a command inside a Pod

```bash
kubectl exec -it <pod-name> -n <namespace> -- <command>
# Example: kubectl exec -it my-pod -n default -- /bin/bash
```

## Create a Pod from a YAML file

```bash
kubectl apply -f <pod-file>.yaml
```

## Delete a Pod

```bash
kubectl delete pod <pod-name> -n <namespace>
```

## Restart a Pod by deleting it (for Pods managed by a Deployment)

```bash
kubectl delete pod <pod-name> -n <namespace>
```

## Filter Pods by label

```bash
kubectl get pods -l <label-key>=<label-value> -n <namespace>
```

## View Pods in a specific state (like "Running" or "Pending")

```bash
kubectl get pods --field-selector=status.phase=<phase> -n <namespace>
```

## View resource usage (CPU/memory) of Pods

```bash
kubectl top pod -n <namespace>
```

## Retrieve the complete YAML of a Pod

```bash
kubectl get pod <pod-name> -n <namespace> -o yaml
```

## View events associated with a Pod

```bash
kubectl describe pod <pod-name> -n <namespace> | grep Events -A10
```

## Force delete a Pod

```bash
kubectl delete pod <pod-name> -n <namespace> --force --grace-period=0
```
