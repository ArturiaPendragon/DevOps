## Notions : Mutable & Immutable

### Définitions

#### Mutable :
- Evolution par Modifications
    - inconvénients :
  - compatibilité/dépendances n'ont pas été testées avant
  - moins adapté sur des infras modernes (cloud, docker...)
  - scalabiltié horzontale lourde
  - rollback moins faciles (dépendances à gérer)
    - avantages :
  - livrables plus légers
  - répartition des rôles plus faciles (dev / ops)

#### Infrastructure Mutable vs Immutable

* immutable:
	- 1 version = 1 package complet
		- exemple : revient à livrer une VM complète
	- on parle aussi d'artefact
	- exemple : image docker
  - inconvénients :
		- packager est plus lourd (automatisation = IAC)
		- développement comprend de l'infrastructure
	  - avantages :
		- itérations facile / rapide (après IAC)
		- versionning global
		- adaptabilité aux environnements nécessaires
		- scalabilité horizontale plus facile
		- rollback plus faciles
