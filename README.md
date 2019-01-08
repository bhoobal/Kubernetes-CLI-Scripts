# Kubernetes-CLI-Scripts

# Kube config

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
 
