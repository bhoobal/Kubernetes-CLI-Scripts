# Kubernetes-CLI-Scripts

# Kube config
kubectl config view
kubectl config current-context
kubectl config use-context k8s.domain.com
kubectl config get-context


example
kubectl config --kubeconfig=config-demo use-context exp-scratch
Note: config-demo -- is a file which has multiple cluste info


#config map
describe config map
kubectl describe cm aws-auth -n kube-system

#get config map
kubectl get cm aws-auth -n kube-system

#apply yaml
kubectl apply -f .\configmap.yaml




#get nodes

#get pods

#get deployment
#get service
# 
kubectl get no
kubectl get po -o wide
kubectl get ns
kubectl get po -o wide -n default
kubectl get po -o wide -n trex
kubectl get po -o wide -n dev
kubectl describe --help

kubectl describe sa

kubectl describe sa -n all-namespaces

kubectl describe sa --all-namespaces

kubectl describe
 kubectl describe roles --help
 kubectl describe roles --all-namespaces
 
 kubectl describe roles --help
 kubectl get clusterroles kubernetes-dashboard-minimal
 
 kubectl get clusterroles
 kubectl get clusterroles admin
 
 kubectl get clusterroles admin -o yaml
 
 kubectl get clusterroles admin -o yml
 
 kubectl get clusterroles admin -o json

Describe specif pod
kubectl get po/chartmuseum-chartmuseum-cf5c7fff-fpr2b -o yaml

List all images

 kubectl get pods --all-namespaces -o jsonpath="{..image}" -o json
 
 kubectl get pods --all-namespaces -o jsonpath="{.items[*].spec.containers[*].image}"
 
 https://kubernetes.io/docs/tasks/access-application-cluster/list-all-running-container-images/
 
 # Installing Helm
 kubectl -n kubernetes-dashboard describe secret admin-user-token


Installing Helm Package
curl https://baltocdn.com/helm/signing.asc | sudo apt-key add -
sudo apt-get install apt-transport-https --yes
echo "deb https://baltocdn.com/helm/stable/debian/ all main" | sudo tee /etc/apt/sources.list.d/helm-stable-debian.list
sudo apt-get update
sudo apt-get install helm


i-pc:/# helm version
version.BuildInfo{Version:"v3.7.2", GitCommit:"663a896f4a815053445eec4153677ddc24a0a361", GitTreeState:"clean", GoVersion:"go1.16.10"}
