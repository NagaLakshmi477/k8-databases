## Databases

mongodb 
-----------
 we will take EBS beacuse it is fast
- to install drivers 
kubectl apply -k "github.com/kubernetes-sigs/aws-ebs-csi-driver/deploy/kubernetes/overlays/stable/?ref=release-1.43"
- adding permissions (ebs)
- create storage class
- we are doing dynamically
kubectl apply -f ebs-sc.yaml
kubectl apply -f 01-namespace.yaml
kubectl apply -f  manifest.yaml
kubectl get pods
kubectl get pvc

redis
-----

horizontal vs vertical auto scaling
----------------------------------
- make sure metrics server is running
- we should mention resources requests and limits

taints and tolerations
-------------------
till now we didn't select the nodes like which need to take the request
now we will select the nodes

kubectl label nodes <IP>.ec2.internal disktype=ssd

taint --> means it is correputed or polluted so we need to re create it means we didn't shudeule any pods here
kubectl taint nodes <ip>.ec2.internal key1=value1:NoSchedule
the node will be in pending state
if you to shudule pods to tainet we can use tolerance
