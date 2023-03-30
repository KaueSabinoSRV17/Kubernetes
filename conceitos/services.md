# Services

Devido ao fato de que Pods são efêmeros e muito frequentemente
desativados, nunca devemos prover acesso direto a eles, e sim
via Serviços. Ele é a ponte entre os Pods e outros Serviços
e consumidores finais.

## Endpoints

Ao criar um Serviço, se cria um Endpoint. Pode ser do tipo:

- ClusterIP: IP virtual acessível apenas pelo Cluster (padrão).
- NodePort: uma Porta que é a mesma em cada node, que também é acessível externamente.
- LoadBalancer: um Load Balancer criado pelo Provedor de Cloud, que vai rotear tráfico externo para cada Node na NodePort.

Estas Opções permitem apenas criar IPs virtuais ou Portas.

### Opções com DNS

É possível também usar Nomes DNS.

- ExternalName: Nome DNS para um Serviço

Vale lembrar que esta opção é apenas disponível com o add-on 
de DNS ativado.

## Definição

Em seu `spec`, devemos especificar uma lista de portas. Cada
uma com o número da porta, e o número da `nodePort`, por exemplo
se estivermos trabalhando com o `type` `NodePort`

**Atenção: as portas dos serviços devem estar entre 30000 e 32767.**
