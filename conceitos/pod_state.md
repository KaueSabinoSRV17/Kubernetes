# Pod State

Os atributos do Estado de um Pod podem ser:

- Pod Status: Status de alto nível.
- Pod Condition: a condição do Pod.
- Container State: a condição do Container em si.

## Status

Ao rodar `get pods` podemos ver o `STATUS` de um Pod.

- Running: Quer dizer que o Pod está rodando e está ligado a um Node.
- Pending: O Pod foi aceito, mas não está rodando.
	- Pode ser devido a uma imagem que ainda está sendo baixada.
	- Se ele não puder ser agendado devido a limitações de hardware, também estará em Pending.
- Succeeded: Todos os containeres do Pod foram terminados com sucesso e não serão restartados.
- Failed: Todos os containeres do Pod foram terminados, e pelo menos um deles retornou um código de falha.
- Unknown: O Status não conseguiu ser determinado.
	- Pode ser devido a um erro de rede.

## Condições

É possível ter um histórico dos Status com `describe pod <nome do pod>`.
Há 5 tipos diferentes de Condições:

- PodScheduled: O Pod foi agendado à um Node.
- Unschedulable: O Pod não pode ser agendado (por exemplo por limitações de hardware).
- Ready: O Pod pode atender requisições e vai ser adicionado aos Serviços
- Inicializado: Todos os containeres foram iniciados com sucesso.
- ContainersReady: Todos os Containeres estão prontos.
