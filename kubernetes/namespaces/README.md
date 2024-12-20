# Commands

## List all namespaces

```bash
kubectl get namespaces
```

## Create a new namespace

```bash
kubectl create namespace <namespace-name>
```

## View details of a specific namespace

```bash
kubectl describe namespace <namespace-name>
```

## Delete a namespace

```bash
kubectl delete namespace <namespace-name>
```

## List resources in a specific namespace

```bash
kubectl get <resource-type> -n <namespace-name>
```

## Set the default namespace for a context

```bash
kubectl config set-context --current --namespace=<namespace-name>
```

## View the current default namespace

```bash
kubectl config view --minify | grep namespace:
```

## List resources in all namespaces

```bash
kubectl get <resource-type> --all-namespaces
```

## Execute a command in a Pod in a specific namespace

```bash
kubectl exec -n <namespace-name> <pod-name> -- <command>
```
