# Commands

## List LimitRanges in a Namespace

```bash
kubectl get limitranges -n <namespace-name>
```

## Get detailed information about a LimitRange

```bash
kubectl describe limitrange <limitrange-name> -n <namespace-name>
```

## Create a LimitRange from a manifest

```bash
kubectl apply -f <file>.yaml
```

## Delete a LimitRange

```bash
kubectl delete limitrange <limitrange-name> -n <namespace-name>
```

## View the resources associated with a LimitRange

```bash
kubectl describe limitrange <limitrange-name> -n <namespace-name> | grep -A 10 "limits"
```
