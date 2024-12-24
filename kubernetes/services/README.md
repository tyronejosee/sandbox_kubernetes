# Commands

## List Services

```bash
kubectl get services
```

## List Services in a specific namespace

```bash
kubectl get services -n <namespace-name>
```

## Get detailed information about a specific Service

```bash
kubectl describe service <service-name>
```

## Create a Service from a manifest

```bash
kubectl apply -f <file>.yaml
```

## Delete a Service

```bash
kubectl delete service <service-name>
```

## View the endpoints of a Service

```bash
kubectl get endpoints <service-name>
```

## Retrieve the YAML of a Service

```bash
kubectl get service <service-name> -o yaml
```

## List Services with additional details

```bash
kubectl get services -o wide
```

## Get information about a Service by port name

```bash
kubectl get services --field-selector spec.ports.name=<port-name>
```
