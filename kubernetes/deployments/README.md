# Commands

## Create a Deployment

```bash
kubectl create deployment <deployment-name> --image=<image-name>
```

## Apply a Deployment from a YAML file

```bash
kubectl apply -f <deployment-file>.yaml
```

## Show all Deployments in the cluster

```bash
kubectl get deployments
```

## Show specific details about a Deployment

```bash
kubectl get deployment <deployment-name>
```

## Get more details about a Deployment (including Pods)

```bash
kubectl describe deployment <deployment-name>
```

## Scale a Deployment

```bash
kubectl scale deployment <deployment-name> --replicas=<number>
```

## Update a Deployment

```bash
kubectl set image deployment/<deployment-name> <container-name>=<new-image>
```

## Delete a Deployment

```bash
kubectl delete deployment <deployment-name>
```

## View the replicas of a Deployment

```bash
kubectl rollout status deployment/<deployment-name>
```

## Rollback Deployment to the previous version

```bash
kubectl rollout undo deployment/<deployment-name>
```

## View the changes of a Deployment (history)

```bash
kubectl rollout history deployment/<deployment-name>
```

## Monitor the Pods of a Deployment

```bash
kubectl get pods -l app=<deployment-name>
# `-l`: label
```
