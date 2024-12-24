# Commands

## Create a Role from a Manifest

```bash
kubectl apply -f <file>.yaml
```

## View Available Roles in a Namespace

```bash
kubectl get roles -n <namespace>
```

## Describe a Specific Role

```bash
kubectl describe role <role-name> -n <namespace>
```

## Delete a Role

```bash
kubectl delete role <role-name> -n <namespace>
```

## Create a RoleBinding from a Manifest

```bash
kubectl apply -f <file>.yaml
```

## View Available RoleBindings in a Namespace

```bash
kubectl get rolebindings -n <namespace>
```

## Describe a RoleBinding

```bash
kubectl describe rolebinding <rolebinding-name> -n <namespace>
```

## Delete a RoleBinding

```bash
kubectl delete rolebinding <rolebinding-name> -n <namespace>
```

## Create a Role Manually from the Command Line

```bash
kubectl create role <role-name> \
  --verb=<verbs> \
  --resource=<resource> \
  -n <namespace>
```

## Create a RoleBinding Manually from the Command Line

```bash
kubectl create rolebinding <rolebinding-name> \
  --role=<role-name> \
  --user=<user-name> \
  -n <namespace>
```

## Check Permissions Associated with a Role

You can use the `kubectl auth can-i` command to check if a user has specific permissions.

```bash
kubectl auth can-i <verb> <resource> -n <namespace> --as=<user>

# kubectl auth can-i list pods -n backend-namespace --as=system:serviceaccount:backend-namespace:pod-and-config-reader-sa
```
