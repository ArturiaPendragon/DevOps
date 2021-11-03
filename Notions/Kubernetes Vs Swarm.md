## Notions : Kubernetes Vs Swarm

#### Que font ces outils ?

* Orchestrateurs de conteneurs
* Mise en place et gestion de cluster docker
* Pool de master (1 ou plus) et des workers (1 ou plus)
* Système intégré de service discovery
* Gestion de réseaux
* Stockage

-------------------------------------------------------------------

####  Quelques points pour comparer

* Installation :
		* swarm : simple et facile avec une seule commande init
		* kubernetes : plusieurs prérequis (swap off, plusieurs packages)

* Command line :
		* swarm : peu de commandes de docker complétées (facile à utiliser et retenir)
		* kubernetes : beaucoup de commandes avec beaucoup d'options (alias indispensable voir plus)

* Monitoring et logs :
		* swarm : ajout manuel, peu de solutions (à l'ancienne), Reimann
		* kubernetes : automatisation possible, ELK, prometheus et grafana

* Scalabilité :
		* swarm : manuel
		* kubernetes : manuel ou hpa (avec des solutions plus poussées)

* Rolling update :
		* swarm : peu de choix de stratégie, pas facile à utiliser (manque l'historique)
		* kubernetes : stratégie personnalisable, historique, rollback facile

* Network :
		* swarm : encryption automatique, facile à configurer, peu de choix
		* kubernetes : plus de choix, plus complexe
