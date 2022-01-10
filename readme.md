install necessary packages
docker
kind
kubectl

create a cluster

kind create cluster


kubectl cluster-info --context kind-kind

then 
copy deploy.yaml file to the instance and type the following command

kubectl create -f deploy.yaml

we can see list of services in
kubectl get svc
kubectl get deployments

to delete deployment or service use
kubectl delete svc svcname
kubectl delete deployment deploymentname

port forwarding to enable public traffic
kubectl port-forward --address 0.0.0.0 service/website 8081:3000