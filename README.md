# Sandbox Kubernetes

## Manifest Structure

### 1. API Version

- **`apiVersion`**: Defines the API version to be used for the resource. Example: `v1`, `apps/v1`, `batch/v1`, etc.

### 2. Kind

- **`kind`**: The type of resource. Examples include:
  - `Pod`
  - `Deployment`
  - `Service`
  - `ReplicaSet`
  - `ConfigMap`
  - `Secret`
  - `Ingress`
  - `Namespace`
  - `PersistentVolume`
  - `StatefulSet`
  - `Job`
  - `CronJob`
  - `DaemonSet`

### 3. Metadata

- **`metadata`**: Information about the resource. Common fields include:
  - **`name`**: The name of the resource.
  - **`namespace`**: The namespace where the resource is located.
  - **`labels`**: Associated labels to organize resources.
  - **`annotations`**: Additional annotations to provide extra information.
  - **`ownerReferences`**: Relationship with other resources (e.g., a Pod linked to a Deployment).
  - **`creationTimestamp`**: Creation timestamp.

### 4. Spec

- **`spec`**: Defines the desired state of the resource. Specific details depend on the type of resource. Examples include:

#### For a Pod

- **`containers`**: List of containers in the pod, each with its configurations such as:
  - **`name`**: Container name.
  - **`image`**: Container image.
  - **`command`**: Command the container should execute.
  - **`ports`**: Ports exposed by the container.
  - **`env`**: Environment variables.
  - **`resources`**: Requested and limited resources (`requests` and `limits`).

#### For a Deployment

- **`replicas`**: The number of Pod replicas the Deployment should create.
- **`selector`**: Label selectors to match Pods managed by the Deployment.
- **`template`**: Template for the Pods created by the Deployment, similar to Pod configuration.
  - **`metadata`**: Labels and annotations for the Pods.
  - **`spec`**: Pod specifications (containers, volumes, etc.).

#### For a Service

- **`ports`**: Ports the service should expose.
- **`selector`**: Labels matching the Pods to which the service should route traffic.
- **`type`**: Service type (e.g., `ClusterIP`, `NodePort`, `LoadBalancer`).

#### For a ConfigMap

- **`data`**: Key-value pairs containing configuration or data.

#### For a Secret

- **`data`**: Similar to `ConfigMap`, but values are base64-encoded and typically contain sensitive information like passwords, certificates, etc.

#### For an Ingress

- **`rules`**: Defines routing rules for services within the cluster.

### 5. Status (Only for created resources)

- **`status`**: Describes the current state of the resource. Typically generated and maintained by the Kubernetes system. Examples:
  - **`availableReplicas`**: Number of available replicas in a Deployment.
  - **`conditions`**: Current conditions of the resource (e.g., `Available`, `Progressing`).

### 6. Resources (Container Resources)

- **`resources`**: Specifies requested and limited resources for containers. Example:
  - **`requests`**: Amount of CPU and memory requested for the container.
  - **`limits`**: Maximum CPU and memory the container can use.

### 7. Volume (Volumes)

- **`volumes`**: Defines the volumes the Pod will use.
- Types of volumes include:
  - `emptyDir`
  - `hostPath`
  - `persistentVolumeClaim`
  - `configMap`
  - `secret`

### 8. Affinity and Tolerations

- **`affinity`**: Controls Pod placement on specific nodes, such as node affinity or Pod affinity rules.
- **`tolerations`**: Allows Pods to run on nodes with specific taints.

### 9. Security Context

- **`securityContext`**: Defines security settings for Pods or containers.
  - **`runAsUser`**: UID under which the container will run.
  - **`runAsGroup`**: GID under which the container will run.
  - **`privileged`**: Whether the container runs with elevated privileges.

### 10. Liveness and Readiness Probes

- **`livenessProbe`**: Checks if a container is alive.
- **`readinessProbe`**: Checks if a container is ready to receive traffic.
  - Both may include configurations like:
    - **`httpGet`**
    - **`tcpSocket`**
    - **`exec`** (command to run inside the container).

### 11. Node Selector

- **`nodeSelector`**: Used to place Pods on specific nodes based on labels.

### 12. Taints and Tolerations

- **`taints`**: Prevent Pods from running on nodes with certain taints unless the Pod has a corresponding toleration.

### 13. Horizontal Pod Autoscaler

- **`minReplicas`** and **`maxReplicas`**: Range of replicas to automatically scale the number of Pods based on load.
