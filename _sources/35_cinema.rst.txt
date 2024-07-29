Cinema roumain
########################
12/7/24

La documentation détaillée du porjet est dans le repo spécific, ici `<https://github.com/dirif25non-partage/cinemaRoumain>`_

L'objectif était d'expérimenter les outils avec un petit groupe d'utilisateurs mais sans utiliser les fonctions d'identification classiques.

Pour suivre les usages, j'ai tenté la capture de l'adresse IP et l'utilisation d'un paramètre de routing spécifique à chaque destinataire des messages d'invisation envoyés.

Mise en oeuvre
***************
:code:`C:\Users\spera\Videos\on\gcp\angular\cine-roumain`

Au départ, les données de 22 films ont été saisies dans un Google Sheet.
Le Sheet est lu par un notebook.
Les données sont placées dans une table Firestore.

Projet fonctionnel
*********************
Créer un site exposant des informations sur le déroulement d'un festival sur le cinéma roumain avec plusieurs pages responsives:

* programme des films présentés (avec résumé du droulement de la séance)
* Listes des films identifiés et possibilité de voter pour les films que l'on veut voir projetés.








