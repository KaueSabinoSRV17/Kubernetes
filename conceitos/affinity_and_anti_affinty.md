# Afinidade e Anti Afiniadde

É uma funcionalidade que nos permite controlar e realizar
agendamentos mais complexos em nossos Nodes e Pods. 

- É uma Linguagem mais expressiva.
- Com ele se cria regras que não são obrigatórias, mas sim uma preferência.

Podemos, por exemplo, garantir que nunca haverão 2 Pods diferentes em um
mesmo Node.

- Afinidade por Node: Semelhante ao nodeSelector.
- Afinidade/Antiafinidade por Pod: Descreve regras sobre como os Pods devem ser agendados, com relação a outros Pods.

Vale lembrar que está funcionalidade só funciona em tempo de Agendamento. 
após um Pod começar a rodar, ele deve ser recreaado para que nocaute.

## Tipos

Há 2 tipos:

- requiredDuringSchedulingIgnoredDuringExecution.
- preferedDuringSchedulingIgnoredDuringExecution.
