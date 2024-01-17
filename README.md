# cbj-kubernetes-files

Change Node password

export KUBECONFIG=/home/guyluz/Documents/kuber/test-kubeconfig.yaml 

kubectl create configmap nginx-config --from-file=nginx.conf


## Configure kubectl (homes-kubeconfig.yaml)
https://www.youtube.com/watch?v=7bA0gTroJjw


## kubectl-cheat-sheet
https://www.digitalocean.com/community/cheatsheets/getting-started-with-kubernetes-a-kubectl-cheat-sheet


Create prod namespace

## pod logs 
kubectl logs

## get pods 
kubectl -n prod get pods

## Aplay pod
kubectl -n prod apply -f home_service.yaml

## Get all pods with name space
kubectl get pods --all-namespaces


## Create name space
kubectl create namespace prod


## get pods ip
kubectl get pods -o wide

## get services
kubectl get services

## list pods on service  (look at endpoint)
kubectl describe services $serviceName

## list all pods (with ip)
kubectl describe pods


Delete
---
## Delete all prod in namespace
kubectl -n prod delete --all pods

## delete service in prod
kubectl -n prod delete --all svc




master - controll the worker nodes orcastra

worker nodes - machine that being controled by the master, hosting multiple pods 

pods - running on worker node 




## delete nginx 
kubectl get pods

kubectl delete deployment nginx-deployment
kubectl delete configmap nginx-config
kubectl delete pods nginx-deployment-5f8fc79b6f-64pmw

## upload
kubectl create configmap nginx-config --from-file=nginx.conf
kubectl apply -f ngnix_deployment.yaml