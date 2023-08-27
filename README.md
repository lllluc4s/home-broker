# HomeBroker DevOps

### Comando para criar o cluster com k3d e executar a aplicação:

```Bash
k3d cluster create meucluster -p "30000:30000@loadbalancer"
```

### Template de rede para o EKS do CloudFormations:

https://s3.us-west-2.amazonaws.com/amazon-eks/cloudformation/2020-10-29/amazon-eks-vpc-private-subnets.yaml

### Comando para obter a senha do administrador no Grafana.

```Bash
kubectl get secret --namespace default grafana -o jsonpath="{.data.admin-password}" | base64 --decode ; echo
```
