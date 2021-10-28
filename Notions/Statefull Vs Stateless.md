## Notions : Statefull Vs Stateless

### Définitions
#### Statefull vs Stateless

* une opposition d'actualité (notamment avec les instances éphémères : docker, compute...)

* s'applique aux applications

* attention il y a aussi les protocoles (SMB = statefull, NFS = stateless)

----

#### Stateless = sans état

* ne conserve pas d'informations liées à une requête ou connexion
* des cookies peuvent permettre de stocker temporairement des données
* très à la mode car très facile à scaler horizontalement (démultiplier le nombre d'instances)
* en gros si infos stockées = côté client ou autres serveurs
ex: applications derrière un LB - stateless = LB possible même avec connexion
* plus d'appels BDD ou API
* facile à reconstruire : on détruit et on recréé

-----------------------------------------------------------------------------------------------
#### Statefull = avec état

* conserve les informations
* scalabilité horizontale impossible
* ne compte pas sur le client pour stocker des infos
* plutôt pour les anciennes applis monolithiques
