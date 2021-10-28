## Notions : Twelve Factors

* Objectif : concevoir des applications comme des services

*Origine : Heroku*

----

#### Liste

* 1 - Base de code : le code à un endroit et versionné (git)
* 2 - Dépendances : outil de gestion des dépendances (maven, composer, leiningen...)
* 3 - Configuration : avoir un fichier de conf pour tous les environnements
avoir recours aux variables d'environnement (cf docker)
* 4 - Services externes : les services doivent être gérés comme des éléments externes
ex : connecteurs BDD
* 5 - Build / Release / Run : ne pas les mélanger (attention dans les pipelines)

--------------------------------------------------------------------------------------

#### Suite
* 6 - Processus : sans état (stateless) doit permettre une scalabilité horizontale

* 7 - Association de ports : les services communiquent sur un port
* 8 - Concurrence : scalabilité horizontale = création de processus plutôt CPU/RAM
* 9 - Jetable : arrêt gracieux et relance sans impact = doit savoir où elle en est
* 10 - Parité dev/prod : intégration des développeurs aux déploiements
* 11 - Logs : flux d'évènement (logstash dans ELK...)
* 12 - Processus d'administration : code admin et applicatif ensemble pas de scission
