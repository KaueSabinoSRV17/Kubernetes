# Skaffold

É uma ferramenta que permite realizar CD de apps que podem
rodar em Kubernetes.

Ele monitora mudanças durante seu desenvolvimento e vai
cuidar de:

- Buildar, com `docker build`.
- Publicar, com o Docker Hub ou outros.
- Deploy para o seu Cluster Kubernetes.

Pode também ser incorporado em seu fluxo existente de 
CI/CD.
