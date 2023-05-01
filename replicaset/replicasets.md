# ReplicaSet

Um ReplicaSet é um gerenciador de um conjunto de réplicas de Pods que estão em execução, porém é recomendado usar um Deployment que gerencie o ReplicaSet.

## Comandos Básicos

### Executar um ReplicaSet através de um arquivo de configuração

```bash
kubectl apply -f <arquivo>
```

### Visualizar todos os ReplicaSets ativos

```bash
kubectl get rs
```

### Checkar o estado do ReplicaSet

Lembrando que o nome do ReplicaSet é definido no `name` do `metadata`.

```bash
kubectl describe <name>
```

### Visualizar os Pods ativos

O ReplicaSet é um gerenciador de Pods, então ele irá gerar Pods.

```bash
kubectl get pods
```

### Escalar manualmente o ReplicaSet

É possível sobrescrever a quantidade de replicas definidas no arquivo de configuração do ReplicaSet, com isso você pode fazer um scaleup ou scaledown.

```bash
kubectl scale rs frontend-rs --replicas=<quantidade-de-pods>
```

### Escalar automaticamente o ReplicaSet

Como é possível escalar manualmente o ReplicaSet, é de se imaginar que seja possível fazer isso de maneira automatizada também.

```bash
kubectl autoscale rs frontend-rs --max=10 --min=3 --cpu-percent=50
```

### Remover um ReplicaSet

```bash
kubectl delete rs frontend-rs
```

## Documentação Oficial

Para uma referencia mais completa, consulte a Documentação oficial do Kubernetes

Link da Documentação: <https://kubernetes.io/docs/concepts/workloads/controllers/replicaset/>
