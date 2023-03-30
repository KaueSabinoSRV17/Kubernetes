# Kubernetes

É uma ferramenta open source de orquestração de containeres, que permite
que múltiplos containeres de serviços longos rodem em uma máquina.

Com todos os containeres rodando, o Kubernetes vai gerenciar o estado do
container, o iniciando em nodes específicos, movendo de um para outro ou
também reiniciar um container caso ele tenha caído.

## Pods

Um Pod descreve uma app no Kubernetes. Em um Pod, podemos ter mais de um
container, mas como boa prática devem ser apenas containeres extremamente
acoplados que sobem uma única aplicação.

### Comandos

#### Get Pod

Lista informações sobre todos os Pods que estão rodando.

	kubectl get pod

#### Describe Pod

Descreve um Pod:

	kubectl describe pod <nome do pod>

#### Expose Pod

Expôe a porta de um Pod e cria um novo serviço:

	kubectl expose pod <nome do pod> --port=<numero da porta> --name=<nome do servico>

#### Port-Foward

Mapeia uma porta da sua máquina para a porta do Pod exposto:

	kubectl port-foward <nome do pod> <numero da porta>

#### Exec

Executa um comando dentro de um container do Pod

	kubectl exec <nome do pod> -- <comando>
