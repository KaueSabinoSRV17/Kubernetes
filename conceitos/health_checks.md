# Health Checks

Se sua App apresentar problemas, o pod e o container podem não parar.
Para garantir que tudo está ok a todos os momentos, você pode rodar
health checks.

É possível fazer o check via linha de comando ou o mais comun:
uma rota HTTP na aplicação.

Toda aplicação de produção deveria implementar Health Checks de alguma
forma, para garantir resiliência e disponibilidade.

**OBS: Caso o seu container morra em casos de erros, um livenessProbe 
não irá fazer muita diferença.**

## Readiness Probe X Liveness Probe

- `livenessProbe`: Indica se um container está rodando.
- `readinessProbes`; Indica se um container está pronto para receber requisições.

Caso o Readiness Probe falhe, o Pod não será reiniciado, mas estará 
fora do Service, para que nenhuma requisição vá para ele enquanto ele 
não está pronto.
