# Kubernetes Commands
 Below are comands to implent the given files


## Pods
* create pod
  * kubectl create -f pods.yml
* see all the pods
  * kubectl get pods
 
 
## Replication Controller
* create replicationController
  * kubectl create -f replication_controller.yml
* list replicationController
  * kubectl get replicationcontroller
* see all the pods
  * kubectl get pods
  
  
## Replica Set
* create replicaset
  * kubectl create -f replica_set.yml
* see the replicaset
  * kubectl get replicaset
* see all the pods
  * kubectl get pods
* edit
  * kubectl edit replicaset replica_set_name
* scale
  * update the replica_set.yml file (change replicas = x)
    * kubectl replace -f replica_set.yml
  * kubectl scale --replicas=x -f replica_set.yml
  * kubectl scale --replicas=x replicaset replica_set_name
* delete
  * kubectl delete replicaset replica_set_name (*Also deletes all underlying Pods)
 
## Namespaces
* create namespace
  * kubectl create namespace namespace_name
  

## Deployment
* create deployment
  * kubectl create -f deployment.yml
  
## View all
* kubectl get all 

## Nodegroup
* create nodegroup
  * eksctl create nodegroup --config-file= nodegroup.yml
* Listing nodegroups
  * eksctl get nodegroup --cluster=<clusterName> [--name=<nodegroupName>]
* scaling
  * eksctl scale nodegroup --cluster=<clusterName> --nodes=<desiredCount> --name=<nodegroupName> [ --nodes-min=<minSize> ] [ --nodes-max=<maxSize> ]
* drain
  * eksctl drain nodegroup --cluster=<clusterName> --name=<nodegroupName>
