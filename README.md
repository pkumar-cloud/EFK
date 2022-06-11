# EFK

```sh
# Clone the EFK repo to K8S mgmt host
git clone git@github.com:pndrns/EFK.git
#k8s objects to be created in this ns as per artifacts yaml file.
kubectl create ns efklog
cd EFK
kubectl create -f .
kubectl get po -n efklog
kubectl get svc -n efklog

# Launch Kibana dashborad using one of the <worker node public ip>:<kibana service node port>
** Add node port to SG of worker node. Same SG is used for all worker nodes.
```

