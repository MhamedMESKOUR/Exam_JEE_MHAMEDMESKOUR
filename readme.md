Projet : Application de gestion des factures
============================================

Ce projet vise à créer une application basée sur une architecture micro-service pour gérer les factures contenant des produits et appartenant à un client.

Travail à faire
---------------

1.  Créer le micro-service `customer-service` qui gère les clients.
2.  Créer le micro-service `inventory-service` qui gère les produits.
3.  Créer la passerelle `Spring cloud Gateway` avec une configuration statique du système de routage.
4.  Créer le service d'annuaire `Eureka Discovery Service`.
5.  Configurer dynamiquement les routes de la passerelle.
6.  Créer le service de facturation `Billing-Service` en utilisant Open Feign.
7.  Créer un client Web Angular (Clients, Produits, Factures).
8.  Déployer le serveur Keycloak :
    -   Créer un Realm.
    -   Créer un client à sécuriser.
    -   Créer des utilisateurs.
    -   Créer des rôles.
    -   Affecter les rôles aux utilisateurs.
    -   Tester les différents modes d'authentification avec Postman en montrant les contenus de Access-Token, Refresh Token.
9.  Sécuriser les micro-services et le frontend Angular en déployant les adaptateurs Keycloak.
10. Ajouter des fonctionnalités supplémentaires de votre choix.

Livrable
--------

Le livrable est un repository Github contenant :

-   Le code source de l'ensemble des micro-services et du frontend.
-   Le rapport montrant les différentes étapes dans le fichier README.MD.

Partie supplémentaire
---------------------

1.  Intégration du Bocker KAFKA.
2.  Création d'un micro-service qui permet de produire aléatoirement des factures et de les publier dans un Topic KAFKA.
3.  Permettre au Micro-service déjà développé `BILLING-SERVICE` de consommer les factures publiées dans le Topic KAFKA et de les enregistrer dans sa base de données.
4.  Créer un micro-service `Data-Analytics-Service` qui utilise l'API KAFKA Streams pour effectuer du Real Time Stream Processing en consommant le streams de facture publiées dans le Topic KAFKA.
5.  Créer une page frontend qui présente en temps réel les courbes produites par le service de Data Analytics.
6.  Déployer l'ensemble des services de l'application en utilisant des conteneurs Docker. Créer les images Docker pour chaque service et le fichier `Docker-compose.yml` qui permet de déployer toute l'application.


Déploiement
-----------

1.  Déploiement des services de l'application avec Docker : Nous allons créer les images Docker pour chaque service et le fichier Docker-compose.yml qui permettra de déployer l'ensemble de l'application.

2.  Exploitation de l'activité pratique N°5 :

    1.  Intégration de Kafka : Nous allons intégrer le système de messagerie Kafka à notre application pour permettre la communication entre différents micro-services.
    2.  Création d'un micro-service de production de factures : Nous allons développer un micro-service qui générera aléatoirement des factures et les publiera dans un Topic Kafka.
    3.  Consommation des factures par le micro-service de facturation : Le micro-service de facturation, déjà développé, consommera les factures publiées dans le Topic Kafka et les enregistrera dans sa base de données.
    4.  Micro-service de Data Analytics : Nous allons créer un micro-service de Data Analytics qui utilisera l'API Kafka Streams pour effectuer du Real Time Stream Processing en consommant le stream de factures publiées dans le Topic Kafka.
    5.  Page Frontend pour la présentation des résultats : Nous allons créer une page frontend qui présentera en temps réel les courbes produites par le service de Data Analytics.

Le livrable final sera un repository Github qui contiendra le code source de l'ensemble des micro-services et du frontend ainsi qu'un rapport dans le fichier README.md montrant les différentes étapes de développement et de déploiement de l'application.


Utilisation
-----------

Pour utiliser ce projet, vous aurez besoin de :

-   Installer et configurer Docker et Docker-Compose sur votre ordinateur
-   Cloner ce repository sur votre ordinateur local
-   Exécuter la commande `docker-compose up` depuis le répertoire racine du projet pour déployer l'ensemble des services
-   Accéder à l'application via un navigateur web à l'adresse `http://localhost:4200`

Dépendances
-----------

Ce projet utilise les technologies suivantes :

-   Java 8 ou plus récent
-   Spring Boot
-   Spring Cloud
-   Angular
-   Kafka
-   Keycloak
-   Docker

Conclusion
----------

Ce projet vous montre comment créer une application basée sur une architecture micro-service pour gérer les factures contenant des produits et appartenant à un client. Les différents micro-services ont été développés avec Spring Boot et ont été déployés avec Docker. Nous avons également intégré Kafka pour permettre la communication entre les différents micro-services et Keycloak pour sécuriser l'application. Enfin, nous avons créé une interface utilisateur avec Angular pour présenter les données gérées par l'application.