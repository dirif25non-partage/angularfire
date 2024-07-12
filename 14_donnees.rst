Méthode d'entrée des données
#################################
mise à jour : 12/7/2024

Liste des méthodes d'entrée
******************************
Fichier .ts
================
Données enregistrée comme une variable dans un fichier qui est importé par les composants.

Plusieurs variables peuvent être enregistrées dnas le même fichier qui peut aussi contenir des interfaces.


Fichier dans assets
====================
Il semble que cela demande de passer par le module HTTP, cela ne me semble pas très utile par rapport à la solution précédente.

`<https://stackoverflow.com/questions/63495923/reading-csv-file-from-a-local-directory>`_

Fichier sur un serveur HTTP comme Google Storage
===================================================
Le fichier est aussi accessible via HTTP, mais il faut que le serveur soit paramétré pour accepter les requêtes "Cross Origin".
Dans le cas, de Google Storage, le paramétrage se fait au niveau du bucket. C'est bien documenté par Google.

Cela peut être utile pour des données de référence qui peuvent être partagées entre plusieurs applications et avec des tiers.

Les données peuvent être mises à jours quotidiennement par une fonction à partir d'une base BigQuery par exemple.

Base Firestore
=================
Cette solution est adaptée à une source de données qui est frequement modifiée.

Le traitement pour placer les données dans une base Firestore est plus lourd, mais la mise à jour des données peut être réalisée par une application.

Le partage des données est limité aux applications à l'intérieur d'un même projet Firebase.

