Visite des issues
***********************
mise à jour 240602


Organisation
=================
Au sein du projet GCP :dett

application :https://issues-de-secours-dirif.web.app/

L'administation des données est faite dans le notebook : configurationIssuesSecours.ipynb

Prochaines étapes
===================
Modifier les questions pour qu'elles correspondent à ce qu'il convient de faire pour une visite simple.

Faire un test avec un PCTT

Développer une autre application pour la visualisation des données.








Projet tel que défini initialiement en avril 2024
====================================================
Faire une application qui permet d'enregistrer les visites et les essais fonctionnels dans les issues.

L'agent se connecte avec son email.

Il sélectionne un tunnel et un numéro d'issue.

il entre les données :

* Facilité d'ouverture de la porte (1,0.5,0)
* Force mesurée avec le dynamomètre (en Newton)
* Taux de luminaires HS (%)
* Fonctionnement de la surpression (1,0.5,0)
* Mesure de la surpression ?
* ...

On produit les tableaux de bord suivants :

* Par tunnel, 

  * date de dernière visite la plus ancienne, 
  * nombre d'issues non visiées depuis 2 mois
  * liste des issues ordonnées selon la date de la dernière visite
* Par PCTT

  * Nombre d'issues visités par mois sur les 12 derniers mois
  * Temps maximum depuis la dernière visite
  * liste des tunnels ordonnés selon la date de la dernière visite
