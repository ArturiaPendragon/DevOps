## Notions : Mesh

---

#### MESH (routing mesh)

* Très tendance avec les microservices, docker et le cloud
* Important pour scaling horizontal
* Utile pour le circuit breaker : éviter les effets "boule de neige"
* Meilleure gestion des retryables

#### Pourquoi ?

*Pet vs Cattle*

* Apprendre à ne pas savoir quel ip porte quel service ?

-> Mise en place d'une registry de service : zookeeper, consul...

---------------------------------------------------------------------------

#### Architecture

* Les outils:

MESH = système registry + reverse-proxy sidecar + service

```
                            +-------------------------+
          +-----------------+  Registry Services      +--------------+
          |                 +-------------------------+              |
    +---------------------------------+        +--------------------------------+
    |     +                           |        |                     +          |
    |   agent            service      |        |    service      ++ agent       |
    |   registry           +          |        |    +            |  registry    |
    |      +               |          |        |    |            |              |
    |      |               +          |        |    +            |              |
    |      |                          |        |                 |              |
    |      +--+ Reverse-Proxy         |        |  Reverse-Proxy  +              |
    |                 ++              |        |        ++                      |
    +---------------------------------+        +--------------------------------+
                      |                                 |
                      +---------------------------------+
                                       ^
                                       |
                                       |
                                    +-----+
                                    |     |
                                    +-----+

```

-------------------------------------------------------------------------

#### Outils

* Reverses-proxies : envoy, linkerd, nginx...
* Registry : consul, zookeeper...
* Package complet : Istio (K8S) = envoy, pilot...

*Définitions* :

* Data plane : tenue à jour du registre
* Control plane : ajout de monitoring, outils de gestion du mesh
