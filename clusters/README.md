# K8s cluster setup
## AWS EKS
### Cluster creation
Follow [eksctl guide](https://docs.aws.amazon.com/eks/latest/userguide/getting-started-eksctl.html) for quickly creating an EKS cluster.

Note: The eksctl cluster create command might fail with below error due to insufficient capacity -
```
AWS::EKS::Cluster/ControlPlane: CREATE_FAILED – "Resource handler returned message: \"Cannot create cluster 'mugdha-test' because us-east-1e, the targeted availability zone, does not currently have sufficient capacity to support the cluster. Retry and choose from these availability zones: us-east-1a, us-east-1b, us-east-1c, us-east-1d, us-east-1f
```
Please use below command instead -
```
eksctl create cluster --name mugdha-test-1 --region us-east-1 --zones us-east-1c,us-east-1d
```
