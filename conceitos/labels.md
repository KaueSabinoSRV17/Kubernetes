# Labels

Labels são valores chave -> valor que podem ser ligados a um
objeto. São como tags nos provedores de Cloud.

Podem ter um grande uso por dentro das definições do Kubernetes,
pois podemos referenciar os Labels de todos os Objetos em outros
Objetos. Isto é chamado de `Label Selectors`.

## Nodes

É possível adicionar labels a Nodes via CLI

	kubectl label nodes <nome do node> <chave do label>=<valor do label>
