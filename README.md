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
