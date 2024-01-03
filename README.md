Run this command to use terraform user.

```bash
aws configure
```

Initialize first and then apply to create an EKS cluster.

```bash
terraform init
terraform apply
```

Before you can connect to the cluster, you need to update the Kubernetes context with the following command:

```bash
aws eks update-kubeconfig --name my-eks --region us-east-1
```

Then a quick check to verify that we can access EKS.

```bash
kubectl get nodes
```