# Kubernetes_Learning

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
