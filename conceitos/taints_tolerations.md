# Taints e Toleration

Podemos estipular o contrário de Afinidade com Toleration,
no caso barrar certos Pods de rodarem em um Node. 

Toleration são aplicadas a um Node, Taints são aplicadas
a um Pod.

Isso pode ser útil por exemplo para que um Pod recém criado 
não vá para o Master.
