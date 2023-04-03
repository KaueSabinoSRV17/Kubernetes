# Auto Scaling

O Kubernetes é capaz de fazer Auto Scaling através de 
métricas. Métricas a nível de aplicação, como quantidade
de queries, também são suportadas.

Ele faz uma querie que mede a utilização de um pod.
Normalmente é uma periodicidade de 30 segundos.

Ele vai usar o Heapster, como ferramenta de monitoramento
para coletar e fazer decisões sobre métricas.

No processo de Autoscaling, podemos definir uma quantia
máxima e mínima de Pods rodando, junto com uma porcentagem
de CPU minimamente desejada. Com base nesta porcentagem, o
cluster vai ter mais ou menos Pods esaaxafa
