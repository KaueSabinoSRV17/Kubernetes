# Secrets

Secrets permitem a distribuiçãode chaves, senhas, credenciais ou qualquer
dado "secreto" para os Pods.

Não são a única forma de conseguir dados sigilisos aos Pods, suas apps
também podem usar Serviços de Vault Externos.

Podem ser usados das seguintes maneiras:

- Variáveis de Ambiente.
- Como um arquivo do pod.
	- Deverá ser usado um volume no cont.ainer
	- Neste volume, estarão os arquivos.
	- Pode ser por exemplo um arquivo `.env`
- Usar uma imagem externa (que deve estar em um registry privado).

## Gerando os Segredos

Para gerar um segredo, é necessário ter um arquivo com o valor sigiloso
e rodar o comando:

	kubectl create secret generic <nome do segrado> --from-file=<caminho até o arquivo com o valor>


