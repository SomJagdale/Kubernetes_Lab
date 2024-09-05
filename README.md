# Kubernetes_Learning
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

