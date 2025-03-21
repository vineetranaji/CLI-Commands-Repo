# Kubernetes Commands

This document provides a list of useful Kubernetes commands for managing Kubernetes clusters.

## Cluster Information and Configuration

### `kubectl config view`
- Displays the kubeconfig file.

### `kubectl config current-context`
- Displays the current context in use by `kubectl`.

### `kubectl config get-contexts`
- Lists all available contexts in the kubeconfig file.

### `kubectl config use-context <context_name>`
- Switches to a different context.

### `kubectl config set-context <context_name> --cluster=<cluster_name> --user=<user_name>`
- Sets a context with the specified cluster and user.

### `kubectl version`
- Displays the client and server versions of Kubernetes.

### `kubectl cluster-info`
- Displays cluster information and the address of the master node.

### `kubectl get nodes`
- Lists all nodes in the cluster.

### `kubectl get namespaces`
- Lists all namespaces in the cluster.

### `kubectl config set-cluster <cluster_name> --server=<server_url>`
- Sets a cluster in the kubeconfig file.

## Pods Management

### `kubectl get pods`
- Lists all pods in the current namespace.

### `kubectl get pods --all-namespaces`
- Lists all pods across all namespaces.

### `kubectl get pods -n <namespace>`
- Lists pods in a specific namespace.

### `kubectl describe pod <pod_name>`
- Displays detailed information about a pod.

### `kubectl logs <pod_name>`
- Displays the logs of a pod.

### `kubectl logs <pod_name> -c <container_name>`
- Displays the logs of a specific container in a pod.

### `kubectl exec -it <pod_name> -- /bin/bash`
- Opens an interactive shell session inside a running pod.

### `kubectl exec <pod_name> -- <command>`
- Executes a command inside a running pod.

### `kubectl delete pod <pod_name>`
- Deletes a pod.

### `kubectl delete pods --all`
- Deletes all pods in the current namespace.

### `kubectl delete pod <pod_name> --grace-period=0 --force`
- Force deletes a pod immediately.

## Deployments and ReplicaSets

### `kubectl get deployments`
- Lists all deployments in the current namespace.

### `kubectl get deployment <deployment_name>`
- Lists a specific deployment.

### `kubectl describe deployment <deployment_name>`
- Displays detailed information about a deployment.

### `kubectl apply -f <file.yaml>`
- Applies the configuration in the YAML file (e.g., creating or updating resources).

### `kubectl create -f <file.yaml>`
- Creates resources defined in a YAML file.

### `kubectl delete deployment <deployment_name>`
- Deletes a deployment.

### `kubectl scale deployment <deployment_name> --replicas=<number>`
- Scales the number of replicas of a deployment.

### `kubectl rollout status deployment <deployment_name>`
- Shows the rollout status of a deployment.

### `kubectl rollout undo deployment <deployment_name>`
- Reverts to the previous version of a deployment.

### `kubectl set image deployment/<deployment_name> <container_name>=<image_name>`
- Updates the image of a container in a deployment.

### `kubectl get replicasets`
- Lists all ReplicaSets in the current namespace.

### `kubectl describe replicaset <replicaset_name>`
- Displays detailed information about a ReplicaSet.

## Services

### `kubectl get services`
- Lists all services in the current namespace.

### `kubectl get service <service_name>`
- Lists a specific service.

### `kubectl describe service <service_name>`
- Displays detailed information about a service.

### `kubectl expose pod <pod_name> --type=LoadBalancer --name=<service_name>`
- Exposes a pod as a service.

### `kubectl expose deployment <deployment_name> --type=LoadBalancer --name=<service_name>`
- Exposes a deployment as a service.

### `kubectl delete service <service_name>`
- Deletes a service.

## Namespaces

### `kubectl create namespace <namespace_name>`
- Creates a new namespace.

### `kubectl delete namespace <namespace_name>`
- Deletes a namespace.

### `kubectl get namespaces`
- Lists all namespaces.

### `kubectl config set-context --current --namespace=<namespace_name>`
- Sets the current namespace for the context.

## Secrets and ConfigMaps

### `kubectl get secrets`
- Lists all secrets in the current namespace.

### `kubectl describe secret <secret_name>`
- Displays detailed information about a secret.

### `kubectl create secret generic <secret_name> --from-literal=<key>=<value>`
- Creates a secret from key-value pairs.

### `kubectl create configmap <configmap_name> --from-file=<file_path>`
- Creates a ConfigMap from a file.

### `kubectl get configmaps`
- Lists all ConfigMaps in the current namespace.

### `kubectl describe configmap <configmap_name>`
- Displays detailed information about a ConfigMap.

## StatefulSets

### `kubectl get statefulsets`
- Lists all StatefulSets in the current namespace.

### `kubectl describe statefulset <statefulset_name>`
- Displays detailed information about a StatefulSet.

### `kubectl delete statefulset <statefulset_name>`
- Deletes a StatefulSet.

### `kubectl apply -f <statefulset_file.yaml>`
- Creates or updates a StatefulSet from a YAML file.

## DaemonSets

### `kubectl get daemonsets`
- Lists all DaemonSets in the current namespace.

### `kubectl describe daemonset <daemonset_name>`
- Displays detailed information about a DaemonSet.

### `kubectl delete daemonset <daemonset_name>`
- Deletes a DaemonSet.

### `kubectl apply -f <daemonset_file.yaml>`
- Creates or updates a DaemonSet from a YAML file.

## Jobs and CronJobs

### `kubectl get jobs`
- Lists all Jobs in the current namespace.

### `kubectl describe job <job_name>`
- Displays detailed information about a Job.

### `kubectl delete job <job_name>`
- Deletes a Job.

### `kubectl apply -f <job_file.yaml>`
- Creates or updates a Job from a YAML file.

### `kubectl get cronjobs`
- Lists all CronJobs in the current namespace.

### `kubectl describe cronjob <cronjob_name>`
- Displays detailed information about a CronJob.

### `kubectl delete cronjob <cronjob_name>`
- Deletes a CronJob.

### `kubectl apply -f <cronjob_file.yaml>`
- Creates or updates a CronJob from a YAML file.

## Horizontal Pod Autoscaling

### `kubectl get hpa`
- Lists all Horizontal Pod Autoscalers in the current namespace.

### `kubectl describe hpa <hpa_name>`
- Displays detailed information about a Horizontal Pod Autoscaler.

### `kubectl autoscale deployment <deployment_name> --cpu-percent=<value> --min=<min_replicas> --max=<max_replicas>`
- Creates an autoscaler for a deployment based on CPU usage.

## Persistent Volumes (PVs) and Persistent Volume Claims (PVCs)

### `kubectl get pv`
- Lists all Persistent Volumes in the cluster.

### `kubectl describe pv <pv_name>`
- Displays detailed information about a Persistent Volume.

### `kubectl get pvc`
- Lists all Persistent Volume Claims in the current namespace.

### `kubectl describe pvc <pvc_name>`
- Displays detailed information about a Persistent Volume Claim.

### `kubectl delete pv <pv_name>`
- Deletes a Persistent Volume.

### `kubectl delete pvc <pvc_name>`
- Deletes a Persistent Volume Claim.

## Ingress

### `kubectl get ingress`
- Lists all Ingress resources in the current namespace.

### `kubectl describe ingress <ingress_name>`
- Displays detailed information about an Ingress resource.

### `kubectl apply -f <ingress_file.yaml>`
- Creates or updates an Ingress resource from a YAML file.

## Logs and Monitoring

### `kubectl logs <pod_name>`
- Displays logs of a pod.

### `kubectl logs -f <pod_name>`
- Displays logs of a pod with follow (live updates).

### `kubectl top pod`
- Displays resource usage (CPU, memory) for pods.

### `kubectl top node`
- Displays resource usage (CPU, memory) for nodes.

## Resource Usage

### `kubectl describe <resource> <name>`
- Displays detailed information about a specific resource (e.g., pod, deployment, node).

### `kubectl get <resource> <name> -o yaml`
- Displays a resource in YAML format.

### `kubectl get <resource> <name> -o json`
- Displays a resource in JSON format.

## Other Useful Commands

### `kubectl version --short`
- Displays a shortened version of the Kubernetes client and server versions.

### `kubectl get all`
- Lists all resources (pods, services, deployments, etc.) in the current namespace.

### `kubectl apply -f <file.yaml>`
- Creates or updates resources defined in a YAML file.

### `kubectl delete -f <file.yaml>`
- Deletes resources defined in a YAML file.

### `kubectl explain <resource>`
- Displays documentation about a specific resource.

### `kubectl rollout history deployment/<deployment_name>`
- Displays the history of a deployment's rollouts.

### `kubectl rollout undo deployment/<deployment_name>`
- Undoes the last rollout of a deployment.

### `kubectl config use-context <context_name>`
- Switches to a specific Kubernetes context.

### `kubectl proxy`
- Starts a proxy server that allows access to the Kubernetes API.

