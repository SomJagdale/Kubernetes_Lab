# Kubernetes_Learning

The **Certified Kubernetes Application Developer (CKAD)** exam focuses on deploying, managing, and troubleshooting applications in Kubernetes. The exam is hands-on and measures practical skills in Kubernetes. Here are some sample questions and tasks that reflect what you might encounter during the CKAD exam:

### 1. **Pod Design**
   - **Question**: Create a pod that runs a `nginx` container and exposes it on port 80.
     - **Task**: Write a YAML manifest for a basic `nginx` pod and ensure it’s running.

   - **Question**: Create a pod that runs two containers: `nginx` and `busybox`. Ensure that the `busybox` container runs the `sleep` command.
     - **Task**: Use a multi-container pod configuration and specify commands for each container.

   - **Question**: Create a pod with a configMap that sets environment variables for the container.
     - **Task**: Define a configMap, and configure the pod to use values from it as environment variables.

### 2. **Multi-container Pods**
   - **Question**: Create a pod that runs two containers: one with `nginx` and another sidecar container that outputs logs to a shared volume.
     - **Task**: Use shared volume and multi-container pod setup to log data from one container to another.

   - **Question**: Create a pod with a `busybox` container that runs continuously and another container that prints messages every 10 seconds.
     - **Task**: Use container `lifecycle` hooks or shared volumes for inter-container communication.

### 3. **Configuration Management**
   - **Question**: Create a `configMap` and mount it as a volume in a pod.
     - **Task**: Create a `configMap`, modify the pod definition to mount the configMap as a file, and ensure the application reads the data from it.

   - **Question**: Create a `secret` and inject it as an environment variable in a pod.
     - **Task**: Create a `Secret` object, then configure the pod to use it as an environment variable.

   - **Question**: Configure a pod with a `configMap` and `secret`. Use the `configMap` for environment variables and the `secret` for sensitive information in a volume.
     - **Task**: Create the necessary resources and configure the pod to mount them.

### 4. **Observability**
   - **Question**: Monitor a running pod and ensure that logs are being correctly written. Forward the logs from a pod to your local machine.
     - **Task**: Use `kubectl logs` and `kubectl port-forward` to view and forward logs.

   - **Question**: Create a pod with a readiness and liveness probe.
     - **Task**: Define the readiness and liveness probes in the pod YAML manifest using HTTP or command-based checks.

### 5. **Services & Networking**
   - **Question**: Create a deployment with 3 replicas of `nginx` and expose it via a ClusterIP service.
     - **Task**: Define a deployment and create a `ClusterIP` service to allow internal communication.

   - **Question**: Create an external service to expose an application to the internet.
     - **Task**: Create a `NodePort` or `LoadBalancer` service and verify external access.

   - **Question**: Define a headless service to enable direct pod communication.
     - **Task**: Create a service without a cluster IP to allow clients to discover pods directly.

### 6. **State Persistence**
   - **Question**: Create a pod that uses a PersistentVolumeClaim (PVC) to store data.
     - **Task**: Define a `PersistentVolume` and `PersistentVolumeClaim`, and configure the pod to mount the PVC as a volume.

   - **Question**: Resize a persistent volume used by a running pod.
     - **Task**: Modify the `PersistentVolumeClaim` to increase the storage size and ensure the pod is updated accordingly.

   - **Question**: Set up a StatefulSet with persistent storage for a database application.
     - **Task**: Define a StatefulSet and configure persistent volumes for each replica to ensure data persistence.

### 7. **Deployments**
   - **Question**: Create a `nginx` deployment with 3 replicas and a rolling update strategy.
     - **Task**: Write a YAML manifest for the deployment and configure the rolling update with zero downtime.

   - **Question**: Scale a deployment from 2 to 5 replicas and verify the changes.
     - **Task**: Use `kubectl scale` to increase the number of replicas and check the running pods.

   - **Question**: Update an existing deployment to use a newer version of an image, ensuring no downtime.
     - **Task**: Use a rolling update strategy to update the deployment and monitor for success.

### 8. **Jobs and CronJobs**
   - **Question**: Create a Kubernetes job that runs a `busybox` container and prints "Hello, Kubernetes!".
     - **Task**: Define a `Job` manifest that runs the command and completes successfully.

   - **Question**: Schedule a `CronJob` to run every day at 8:00 AM and output "Backup completed".
     - **Task**: Write a `CronJob` manifest that schedules the command and monitors it.

### 9. **Application Lifecycle Management**
   - **Question**: Create a deployment and configure a horizontal pod autoscaler (HPA) that scales the deployment when CPU usage exceeds 70%.
     - **Task**: Set up the deployment and configure HPA using `kubectl autoscale`.

   - **Question**: Create a deployment with an init container that waits for a service to become available before starting the main container.
     - **Task**: Define an init container and ensure it waits for a specific condition before starting the main application container.

### 10. **Security Contexts**
   - **Question**: Create a pod that runs with a non-root user.
     - **Task**: Define a `securityContext` in the pod manifest to run the container with a specific user ID.

   - **Question**: Define a security context for a pod that denies access to privileged containers.
     - **Task**: Write a YAML file with `securityContext` settings that restrict privileged access.

   - **Question**: Limit CPU and memory usage for a pod using resource requests and limits.
     - **Task**: Configure a pod manifest to define resource requests and limits for CPU and memory.

### 11. **Accessing Applications**
   - **Question**: Expose a Kubernetes deployment using a `NodePort` service and ensure it is accessible externally.
     - **Task**: Define the service, expose the deployment, and verify external access using the `NodePort`.

   - **Question**: Use an ingress resource to expose multiple services via a single external IP.
     - **Task**: Define the ingress resource and configure it to route traffic to different services based on path or host.

### 12. **Basic Troubleshooting**
   - **Question**: A pod is not starting due to a crash loop. Use `kubectl logs` to troubleshoot and fix the issue.
     - **Task**: Investigate the logs, determine the root cause, and resolve the issue (e.g., by updating the container’s command).

   - **Question**: A service is not reachable within the cluster. Use `kubectl describe` to troubleshoot the issue.
     - **Task**: Diagnose potential issues like misconfigured endpoints or network policies and resolve them.

   - **Question**: A deployment is failing to scale due to insufficient resources on the nodes. Adjust the resource requests or limits.
     - **Task**: Modify the deployment’s resource requests and limits, or increase the cluster’s resources if needed.

### 13. **Advanced Scheduling**
   - **Question**: Schedule a pod on a specific node using a nodeSelector.
     - **Task**: Define a `nodeSelector` in the pod specification to ensure it runs on a particular node.

   - **Question**: Use taints and tolerations to prevent a pod from running on a specific node.
     - **Task**: Apply a taint to the node and configure the pod’s tolerations accordingly.

### Key Focus Areas:
- **Configuration and Secrets**: Managing `ConfigMaps` and `Secrets` for environment variables and volumes.
- **Pod Design and Multi-Container Pods**: Design pods that perform specific tasks or work together.
- **Observability**: Use logging, readiness/liveness probes, and monitoring tools.
- **Application Lifecycle Management**: Use deployments, jobs, and CronJobs for managing the application lifecycle.
- **Networking**: Work with services, ingresses, and networking policies to expose and secure applications.
- **Security Contexts**: Apply security controls to pods and containers, such as running non-root containers.


kind: Secret and kind: Opaque
kubeconfig file is used by both kubectl and Helm to interact with Kubernetes clusters

kubectl cluster-info

~/.kube/config

cd ../

~/.kube

mkdir .kube

cp Downloads/testk8s.config  ~/.kube/config

kubectl get nodes

sudo snap install helm

sudo snap install helm --classic

helm

kate .kube/config 

kubectl create namespace mobileum-dev

kubectl get pods

helm install myapp -f /home/somnath/Downloads/myapp.yaml myapp

helm dependency build myapp

helm install myapp -f /home/somnath/Downloads/myapp.yaml myapp

helm list

helm uninstall myapp

kubectl get pods -w

kubectl get secrets

helm dependency build myapp

helm dependency update myapp

helm install myapp -f /home/somnath/Downloads/myapp.yaml myapp

kubectl exec -it myapp-0 -- sh

helm upgrade myapp -f /home/somnath/Downloads/myapp.yaml myapp

kubectl logs myapp-0

kubectl describe pod myapp-0


kubectl cluster-info

~/.kube/config

cd ../

~/.kube

mkdir .kube

cp Downloads/testk8s.config  ~/.kube/config

kubectl get nodes

sudo snap install helm

sudo snap install helm --classic

helm

kate .kube/config 

kubectl create namespace mobileum-dev

kubectl get pods

helm install myapp -f /home/somanath/Downloads/myapp.yaml myapp

helm dependency build myapp

helm install myapp -f /home/somanath/Downloads/myapp.yaml myapp

helm list

helm uninstall myapp

kubectl get pods -w

kubectl get secrets

helm dependency build myapp

helm dependency update myapp

helm install myapp -f /home/somanath/Downloads/myapp.yaml myapp

kubectl exec -it myapp-0 -- sh

helm upgrade myapp -f /home/somanath/Downloads/myapp.yaml myapp

kubectl logs myapp-0

kubectl describe pod myapp-0


kubectl get nodes

kubectl get pods

kubectl get services

kubectl get deployments

kubectl get namespaces

kubetl get/describe/delete nodes/pods/services/deplyments/namespaces

kubectl apply -f values.yaml

kubectl create -f <filename>

kubectl create namespace <namespace-name>

kubectl logs <pod-name>

kubectl logs -f <pod-name>  # Follow logs

kubectl scale deployment <deployment-name> --replicas=<number>

kubectl expose pod <pod-name> --type=<service-type> --name=<service-name>

kubectl get services

kubectl create configmap <configmap-name> --from-literal=<key>=<value>

kubectl create secret generic <secret-name> --from-literal=<key>=<value>

kubectl get roles

kubectl get clusterroles

kubectl get rolebindings

kubectl get clusterrolebindings

kubectl config current-context

