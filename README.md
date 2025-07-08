# Test technique

## Objectifs
Développer une API REST permettant de créer et supprimer des clusters en suivant le principe du storage first.

## Outils disponibles
- fichier Open API contenant la description des différents endpoint à implémenter
- fichier docker-compose pour monter une base mongo (interface graphique mongo-express sur le port 8081)

## Contraintes
- un utilisateur = un tenant, un tenant ne doit voir que les clusters lui appartenant.
  (pour simplifier, le tenant sera passé en header de la requête HTTP sous forme de chaîne de caractères)
- la mise à jour des opérations asynchrones est faite directement en base par un processus externe
- la base de donnée utilisée est une base mongo (à monter via docker-compose)
- langage et framework : fastapi en python + toute bibliothèque jugée utile.
- l'exécutable de l'API devra pouvoir être dockerizé pour pouvoir être déployé sur Kubernetes

## Livrables
 - code sur repo github avec Readme pour procédure de build/test
 - docker-compose pour lancer la BDD + API
 - date limite 16 juillet