# Java-App-Deployment-on-Kubernetes-Cluster
Java App Deployment on Kubernetes Cluster

![image](https://user-images.githubusercontent.com/96833570/223191176-9e92e255-5343-418f-a7bc-c8f6d5e34602.png)


### Creating the Cluster

```
  export KOPS_STATE_STORE="s3://kops-bucket-rrrandom"
  export MASTER_SIZE="t3.medium"
  export NODE_SIZE="t3.small"
  export ZONES="us-east-1a"
  kops create cluster k8s.devtechops.dev\
  --node-count 2 \
  --zones $ZONES \
  --node-size $NODE_SIZE \
  --master-size $MASTER_SIZE \
  --master-zones $ZONES \
  --yes
 ```

```
kops update cluster --name k8s.devtechops.dev --yes
kops validate cluster --name  k8s.devtechops.dev --state=s3://kops-bucket-rrrandom

aws ec2 create-volume \
    --volume-type gp2 \
    --size 3 \
    --availability-zone us-east-1a
```


```
kubectl get nodes --show-labels
kubectl get nodes
kubectl describe node ip<>
kubectl label nodes ip<> zone=us-east-1a

kubectl create -f secret.yaml
kubectl get secret
kubectl describe secret


 kubectl create -f dbdep.yaml
 kubectl create -f .
 
 ```






![image](https://user-images.githubusercontent.com/96833570/223102623-367e9989-d5a9-4a18-8df8-aac9f1210e18.png)


![image](https://user-images.githubusercontent.com/96833570/223103589-e8697e83-31e3-430e-9a56-707c1de3a357.png)

![image](https://user-images.githubusercontent.com/96833570/223103697-7dbc23c7-e69a-49b1-b13e-ca44d62b1b96.png)


## Validation


https://user-images.githubusercontent.com/96833570/223153579-8c03c26e-b2c9-42a5-ab66-17b8a59ca592.mp4

