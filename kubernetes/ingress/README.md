# Commands

## List all Ingress resources

```bash
kubectl get ingress
```

## List Ingress in a specific namespace

```bash
kubectl get ingress -n <namespace>
```

## Get details of a specific Ingress resource

```bash
kubectl describe ingress <ingress-name>
```

## Create an Ingress from a YAML file

```bash
kubectl apply -f <ingress-file.yaml>
```

## Update an Ingress

```bash
kubectl apply -f <ingress-file.yaml>
```

## Delete an Ingress

```bash
kubectl delete ingress <ingress-name>
```

## View events related to an Ingress

```bash
kubectl describe ingress <ingress-name>
```

## View the rules of an Ingress in YAML/JSON format

```bash
kubectl get ingress <ingress-name> -o yaml
kubectl get ingress <ingress-name> -o json
```

## Check the endpoints of related services

```bash
kubectl get endpoints
```
