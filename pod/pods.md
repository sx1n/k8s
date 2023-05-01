# Pods

São os menores Objetos do Kubernetes, Um pod é um grupo de um ou mais containers, com recursos
de armazenamento, rede compartilhada e uma especificação de como executar os contêineres.  

**Lembrando que adicionar mais de um container em um pod, pode ser um caso de uso mais avançado.**

## Comandos Básicos

### Executar um Pod através de um arquivo de configuração

Lembrando que se o Pod estiver ativo, ele será alterado com base nas configurações do arquivo.

```bash
  kubectl apply -f <arquivo>
```

### Visualizar todos os Pods ativos

```bash
  kubectl get pods
```

### Deletar um Pod

```bash
  kubectl delete pod <nome-do-pod>
```

Também é possivel deletar varios pods de uma só vez.

```bash
  kubectl delete pods <nome-dos-pods>
```

## Documentação Oficial

Para uma referencia mais completa, consulte a Documentação oficial do Kubernetes.

Link da Documentação: <https://kubernetes.io/docs/concepts/workloads/pods/>
