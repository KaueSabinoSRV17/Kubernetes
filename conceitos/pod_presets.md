# Pod Presets

Pod Presets podem injetar informações para dentro de um Pod
em Runtime. Estas informações são Recursos do Kubernetes,
como Secrets, ConfigMaps, Volumes e Variáveis de Ambiente.

No caso, ele pode ser usado para automatizar essa tarefa para 
diversos apps que você vai deployiar.

Caso haja conflito, não serão aplicados os Presets.
