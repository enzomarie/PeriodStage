# Analyse et Schématisation des représentations des périodes historiques

## Analyse du réel

### Schématisation PeriodO

Les données sont assez simples à visualiser et l'organisation et l'ontology sont facile à synthétiser. Voir les feuilles.

### Schématisation Wikidata

Très compliquée, enfaite il y a une classe période historique, mais qui “syntaxiquement” ou plutôt dans la modélisation, est un objet similaire à la “Préhistoire” par exemple. Les relations de domination ou d’appartenance ne se font que par propriétés. Enorme difficulté de visualisation, une objet peut être une classe et une instance en même temps est pas commun pour moi.  Donc c’est compliquée d’avoir les ontologies correspondantes aux périodes historiques, et de faire une modélisation assez exhaustive. Certaines périodes historiques utilise certaines indicateurs temporels, et certaines en utilisent d’autres. 

### Différences notables 

Les différences notables entre les deux ontologies sont multiples. Un des points de différence majeur est le regroupement des terminologies . Dans PeriodO, la totalité des informations qu’une source décrit devient une instance même du graphe, donc si plusieurs auteurs/autrices définissent la même chose, cette période sera en plusieurs fois dans le graphe de connaissances. Dans WikiData, j’ai plutôt l’impression que ça a été regrouper, comme un consensus, en une seul concept et les différentes sources sont décrites par une propriété qui “liste” les sources.  Cela permet une meilleur organisation, mais certaines variations peuvent être supprimer, même si elles sont utilisés. 

Ce que Wikidata a en plus aussi c’est la modélisation continue, c’est à dire les propriétés permettant de situer dans le temps une période historique en fonction des autres périodes historiques, avec des propriétés comme follows, followed by, subclassOf ou partOf. 

Les deux ontologies possèdent des notions d’incertitude par rapport aux intervalles de temps d’une période historique. 

La lisibilité et la compréhension de WikData est atroce et impossible. Il n’y a pas d’explication lié aux périodes historiques, et on permet également à des instances de périodes historique d’ajouter certaines propriétés, sachant que la propriété d’instanciation n’impose rien quand aux nécessités qu’une période historique doit avoir.