## Notions : Intérêt des microservices

#### Cet intérêt des microservices ?

*Concept utilisé dans la plupart des entreprises ou l'IT
est à la pointe : Netflix, Sarenza, Amazon, Google...*

----
#### Pourquoi ?

* périmètres restreints = plus petites équipes (pizzas)
* développement plus simple, plus rapide, plus agile
* versions plus faciles à itérer (devops)
* plus facile à tester
* base de données plus réduites moins complexes... moins sql
* meilleure gestion des défaillances : LB, circuit breaker, cache

----------------------------------------------------------------------

#### Inconvénients

* gérer les flux entre des centaines de microservices
* sollicitation plus importante des réseaux
* infrastructure plus complexe
* création de registry de services (cf consul, zookeeper...)
* communication par API : organiser, standardiser, normer
* bonne communication entre les équipes : devs, infras, devops...
* effet de mode adapté aux technos actuelles (docker, cloud...)
