# Volumes

Volumes permitem rodar aplicações com estado no Kubernetes.
Esse tipo de aplicação pode ter um banco de dados, arquivos,
etc.

Em volumes, os arquivos e dados podem ser persistidos, de forma que,
caso um container morra e outro o substitua, ele terá os mesmos dados
do volume disponíveis.

Os volumes devem ser criados em um Pod.
