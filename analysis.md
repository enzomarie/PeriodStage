# Analyse des représentations des périodes historiques

### Schématisation PeriodO

Les données sont assez simples à visualiser et l'organisation et l'ontology sont facile à synthétiser. Voir les feuilles.

### Schématisation Wikidata

Très compliquée, enfaite il y a une classe période historique, mais qui “syntaxiquement” ou plutôt dans la modélisation, est un objet similaire à la “Préhistoire” par exemple. Les relations de domination ou d’appartenance ne se font que par propriétés. Enorme difficulté de visualisation, une objet peut être une classe et une instance en même temps est pas commun pour moi.  Donc c’est compliquée d’avoir les ontologies correspondantes aux périodes historiques, et de faire une modélisation assez exhaustive. Certaines périodes historiques utilise certaines indicateurs temporels, et certaines en utilisent d’autres. 

### Différences notables 

Les différences notables entre les deux ontologies sont multiples. Un des points de différence majeur est le regroupement des terminologies . Dans PeriodO, la totalité des informations qu’une source décrit devient une instance même du graphe, donc si plusieurs auteurs/autrices définissent la même chose, cette période sera en plusieurs fois dans le graphe de connaissances. Dans WikiData, j’ai plutôt l’impression que ça a été regrouper, comme un consensus, en une seul concept et les différentes sources sont décrites par une propriété qui “liste” les sources.  Cela permet une meilleur organisation, mais certaines variations peuvent être supprimer, même si elles sont utilisés. 

Ce que Wikidata a en plus aussi c’est la modélisation continue, c’est à dire les propriétés permettant de situer dans le temps une période historique en fonction des autres périodes historiques, avec des propriétés comme follows, followed by, subclassOf ou partOf. 

Les deux ontologies possèdent des notions d’incertitude par rapport aux intervalles de temps d’une période historique. 

La lisibilité et la compréhension de WikData est atroce et impossible. Il n’y a pas d’explication lié aux périodes historiques, et on permet également à des instances de périodes historique d’ajouter certaines propriétés, sachant que la propriété d’instanciation n’impose rien quand aux nécessités qu’une période historique doit avoir.

### OWL-Time

Cette ontologie permet de modéliser vraiment la temporalité d’une manière assez exhaustive. Il y a trois grandes famille de classe pour moi : les **durées**, les **intervalles**, les **instants** . Un durée est juste une indication sur la durée d’un événement, sans aucune position temporelle. C’est sans doute bien de le couplet avec des intervalles pour représenter le flou d’une période. Les intervalles sont modélisée par *ProperInterval*, qui est un intervalle d’une durée > 0. Mais ce qui est pas mal avec ça c’est que un algèbre (d’Allen) est disponible dessus, où l’on permet de situer relativement une période avec une autre, ce qui est très important. Quand aux *Instants*, ils représentent des points temporels (sans durée), qui repose sur un SRT (système de référence temporel, par défaut le calendrier grégorien, mais que l’on peut changer dans pas mal de système différent), et cela permet de représenter (par *DateTimeDescription* souvent) un instant dans l’histoire. Même si, dans le pragmatisme mathématique, un instant est toujours un intervalle (car le temps est continue), notre utilisation permet de bien distinguer les deux. 

### Intégration par rapport à l’article

Le problème avec nos représentations, ce sont bien sûr l’absence d’incertitude ou de flou. Dans certaines périodisations, comme une périodisation en rapport avec l’économie, la technologie, ou d’autres fait qui se répandent dans le temps. Owl-time et donc WikiData et PeriodO modélisent le flou avec un intervalle, mais cette intervalle à aussi un début et une fin (des instants du coup). Ce qui veut dire que il y a encore une barrière brute entre avant cette intervalle, et après le début de l’intervalle. Or ce que l’article décrit, c’est que les “dates” peuvent n’être uniquement des consensus d’historiens, qui représentent le changements mais qui n’est pas réellement le jour “où tout a basculé). La notion de continuité peut être importante, et une modélisation probabiliste ou fonctionnelle peut être vraiment bien ici, pou r représenter l’intensité du changement.

Ce que l’article explique aussi, c’est la pluralité de définitions ou de différence que peut avoir un période même ou un terme historique, qui peut différer en fonction du lieu où cela se trouve ou même juste des débats entre historiens qui sont pas d’accord. Pour ce cas-ci, un mélange entre WikiData et PeriodO est nécessaire, car PeriodO apporte énormément de redondance et parfois de logique un peu foireuse, par le manque de lien entre les différentes sources d’informations, et WikiData englobe tout sous le même “terme”, donc supprime la notion de désaccord. Ainsi le mieux serait de trouver un entre deux, peut-être qui regroupe une notion en une même entité, mais donc que l’on peut faire de la multi-définition (et qui doit englober un certain nombre de chose, avec du shacl).