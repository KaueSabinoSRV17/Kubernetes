# Microserviços

O Kubernetes é perfeito tanto para apps Monolíticas quanto
para Microserviços. 

Quando estamos trabalhando com Microserviços nós vamos ter
os seguintes problemas:

- Não há encriptaçao entre apps.
- Apps não tentam se contectar mais de uma vez.
- Não há Loadbalancing entre Apps.

No Kubernetes, se usa o padrão Istios para implantar
Microserviços.

## Soluções

Para todos os problemas apresentados, temos algumas
soluções:

- Sidecar: Um Proxy para cada Microserviço (Dados Encripatados, Loadbalancing Inteligente).
- Interfaces de Gerenciamento: Decisões de Roteamento, Logs, Controle de Acesso.

## Segurança

No istios, temos segurança por default, ou seja, não é
necessário implementar nada extra em nossos apps que já
estão prontos, já que se usa o padrão Sidecar.

Se usa sistemas de segurança já existentes para proporcionar
múltiplas camadas de defesa. Além disso, por padrão a Rede
não tem liberação nenhuma.

Vale ressaltar que os Microserviçoes também não terão acesso
a redes externas (se necessário, devemos ativar o Egress
Traffic).

### Tipos

- Transport Auth: de Serviço para Serviço usando TLS mútuo.
- Origin Auth: Autenticação do usuário final (JWT).
- RBAC: É possível determinar Roles para os Microserviços.
