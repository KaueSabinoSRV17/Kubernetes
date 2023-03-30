# DNS Externo

Ao usar a opção de Ingress do Kubernetes, podemos diminiur
os nossos custos com Load Balancers, usando apenas um para
capturar todo o tráfego externo e o enviar para o Controller
Ingress. 

Vale lembrar que isso só vai funcionar para apps baseadas em
HTTP.

Podemos habilitar a opção `External DNS` do Kubernetes para 
que sejam criados automaticamente todos os DNS Records no 
nosso provedor de DNS (por exemplo o route53).
