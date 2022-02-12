# Documentation du projet

## Qu'est-ce que Docker ?

Pour commencer, Docker est un logiciel permettant de lancer des applications dans des conteneurs logiciels. 
Un conteneur permet aux développeurs d'isoler les applications de leur environnement. En effet, un conteneur enveloppe une application et ses dépendances de façon à les isoler pour les exécuter sur n'importe quel serveur.

Les points forts de Docker sont sa flexibilité et sa légèreté. En effet, les conteneurs Docker sont construits à partir des images Docker (quelques MB au minimum) et permettent aux développeurs de créer, déployer et exécuter efficacement des applications distribuées.

Cependant, il ne faut pas confondre la virtualisation et la conteneurisation. La conteneurisation est une forme plus légère qui s'appuie sur certaines parties de la machine hôte pour fonctionner.

![alt text](https://github.com/Tomston/Bouton_Thomas_SRB_2022_Docker/blob/main/Image.png)

Pour finir, les conteneurs permettent à une application d'être empaquetée et déplacée facilement, augmentant ainsi la simplicité d'une infrastructure.

> **Note** : https://fr.wikipedia.org/wiki/Docker_(logiciel)


## Fonctionnement de Docker

Le principe de fonctionnement de Docker est simimaire à celui de LXC :
1. Des coneneurs en cours d'exécution partagent le même noyau Linux, ce qui les rend plus léger que des machines virtuelles.
2. Des conteneurs en cours d'exécution sont isolés les uns des autres et on uniquement accèes à une quantité limitée de ressources système.

> **Note** : https://www.ionos.fr/digitalguide/serveur/know-how/quest-ce-que-docker/

![alt text](https://github.com/Tomston/Bouton_Thomas_SRB_2022_Docker/blob/main/Image2.png)

> **Note** : LXC est un système de virtualisation utlisant l'isolation comme méthode de cloisennement au niveau du système d'exploitation. Alors qu'un conteneur est un système logiciel.

Docker utilise le noyau Linux et des fonction de ce noyau pour séparer les processus afin qu'ils s'exécutent de façon independante.
Le but de cette séparation est d'optimiser l'utilisation de notre infrastructure, tout en bénéficiant du même niveau se sécurité que celui des systèmes distincts.

> **Note** : https://www.redhat.com/fr/topics/containers/what-is-docker#comment-fonctionne-la-technologie-docker


## Architecture du projet

Voici l'architecture du projet : 
![alt text](https://github.com/Tomston/Bouton_Thomas_SRB_2022_Docker/blob/main/Image3.png)

Voici la liste des systèmes d'exploitation :
* Application : *Alpine Linux*
* API : *Alpine Linux*
* Base de données : *Compatible avec Linux, Windows et Mac*

De plus, voici ci-dessous la liste des ports utilisés :
* Port 3000: *utilisé par l'application*
* Port 8080: *utilisé par l'API rest*
* Port 27017: *utilisé par la base de données*

## Fonctionnement de l'architecture

L'application Node.js devra authentifier un utilisateur déjà inscrit et lui donner accès à un feed utilisateur

Depuis le navigateur Web, nous pouvons nous inscrire en renseignant une adresse mail, un nom d'utilisateur et un mot de passe (avec au moins un majuscule, un chiffre et un caractère spéciale) comme ci-dessous :

![alt text](https://github.com/Tomston/Bouton_Thomas_SRB_2022_Docker/blob/main/Image4.png)

En parallèle, le serveur exécute l'api

À ce moment là, l'API rest transmettra les données à la base de données (MongoDB) afin que celle-ci enregistre les données dans sa base.

Ensuite, nous renseignons notre mail et notre mot de passe que nous avons créons à l'étape précédente :

![alt text](https://github.com/Tomston/Bouton_Thomas_SRB_2022_Docker/blob/main/Image5.png)

La connexion est établi et nous pouvons publier un post :

![alt text](https://github.com/Tomston/Bouton_Thomas_SRB_2022_Docker/blob/main/Image6.png)

> **Note** : https://www.redhat.com/fr/topics/api/what-is-a-rest-api

## Fonctionnement des Dockerfile

![alt text](https://github.com/Tomston/Bouton_Thomas_SRB_2022_Docker/blob/main/Image7.png)

## Fonctionnement du docker-compose.yml
