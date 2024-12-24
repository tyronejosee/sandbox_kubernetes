# Commands

## List ClusterRoles

```bash
kubectl get clusterroles
```

## Get detailed information about a specific ClusterRole

```bash
kubectl describe clusterrole <clusterrole-name>
```

## Create a ClusterRole from a manifest

```bash
kubectl apply -f clusterrole.yaml
```

## Delete a ClusterRole

```bash
kubectl delete clusterrole <clusterrole-name>
```

## List ClusterRoleBindings

```bash
kubectl get clusterrolebindings
```

## View a ClusterRoleBinding

```bash
kubectl describe clusterrolebinding <clusterrolebinding-name>
```

## Create a ClusterRoleBinding

```bash
kubectl apply -f <file>.yaml
```

## Delete a ClusterRoleBinding

```bash
kubectl delete clusterrolebinding <clusterrolebinding-name>
```

## View the permissions of a ClusterRole

```bash
kubectl describe clusterrole <clusterrole-name> | grep -A 10 "Rules"
```

## List roles and bindings for a specific namespace

```bash
kubectl get clusterrolebindings --namespace=<namespace-name>
```
