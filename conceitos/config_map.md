# Config Map

Parâmetros de Configuração que não são segredos podem ser colocados 
em um Config Map.

Mais uma vez, são pares de chaves e valores.

Podem ser lidos pelo app através de:

- Variáveis de ambiente.
- Argumentos de linha de comando do Container na configuração do Pod.
- Usando volumes.

 Um ConfigMap pode conter todo um arquivo de configurações,
 por exemplo uma config do Nginx.

 Esse arquivo pode ser montado com um volume no lugar que a app 
 espera que haja o arquivo de config.
