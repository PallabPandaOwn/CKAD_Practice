# CKAD Exam
 Certified Kubernetes Administrator
- CKAD practices session 
- CKAD Theories

Service
1.  Types of services
    1.  NodePort
    2.  ClusterIP
    3.  LoadBalancer

ClusterIP is the default type service by default.

At time of kubernetes cluster creation , kubernetes will only one service in default namespace called 'kubernetes'

Namespace -:
1. Default namespace - default
2. kube-system namespace - internal services and pod
3. kube- public namespace - resources available for public

kubectl create namespace <name>
Assign quota resources to namespace
DNS url - : db-service.dev.svc.cluster.local 


## Imperative vs Declarative approaches
    1.Imperative -: Step by step instruction 
        -   kubectl create,run,expose,edit,scale - these are imperative commands
        -   These are hard to remember
        -   only available for user session
    2.Declarative -: Just a single instruction
        -   Infrastructure As Code is declarative approaches
        -   kubectl apply -f <definition.yml file>
        -   

  While you would be working mostly the declarative way – using definition files, imperative commands can help in getting one time tasks done quickly, as well as generate a definition template easily. This would help save considerable amount of time during your exams.


## Scheduling
 1. Manual Scheduling - if there are no scheduler is running
 2. If Scheduler is running then it will select the correct pod for pod.

## Taint and Toleration
1.  Taint will be setup on Node and Toleration will be setup in pod 

    -  kubectl taint node <name> key=values:effect
       1. kubectl taint node node1 spray=mosquito:NoSchedule
       2. kubectl get pod --watch
       3. kubectl taint node node1 spray=mosquito:NoSchedule--

