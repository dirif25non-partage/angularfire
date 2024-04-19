Caractéristiques des tunnels (3/24)
*************************************
Objectifs
==========
Il s'agit de mettre à disposition sur smartphone des données (longueur, TMJA, code,nom ...) sur les tunnels et les DS.
Les utilisateurs n'ont que des droits de lecture, ce qui évite de passer par l'authentification.

Il y a un lien avec le projet de faire un référentiel sur les tunnels.

Choix fonctionnels
====================
Pour la liste des DS, je suis parti du tableau de suivi de PBD/CL mais je constate des inconsistances, certains DS passés ensembles sont fusionnés alors que d'autres sont dissociés.
La logique serait de dissocier les DS passés ensemble de même que l'on dépose bien 2 dossiers différents.

Pour les tunnels élémentaires j'ai repris la décomposition précédente mais je ne considère pas que cela soit satisfaisant. La principale difficulté concerne l'échangeur A14/A86. 

A la réflexion, je pense que l'enjeu de clarifier la composition de cet échangeur pousse à considérer les bretelles commes des tunnels élémentaires.



Déroulement
=============
Après de nombreux essais infructueux en février et mars 2024 ...
Il s'agit de la première expérience réussie d'intégrer Angular, Matérial table et Firestore dans une application.
Cela m'a permis de maitriser des notions pratiques de base sur la syntaxe d'Angular.

Organisation
==============
On utilise le compte exploit.diridf et le projet tunnels (:code:`id:tunnels-dirif`).

Les données d'entrées (table des DS et des tunnels) sont traitées par un notebook : `Referentiel tunnels.ipynb <https://colab.research.google.com/drive/1FDtybG180Ik4Y09r8htxegNa_KVWhzmG?authuser=4#scrollTo=t3g3QZrEk0Wd>`_. 

Il est possible d'utiliser l'API de Firestore depuis le notebook pour alimenter la base de données.

Pour le développement de l'application, j'ai travaillé sur CloudShell :code:`exploit_diridf@cloudshell:~/tunnels (tunnels-dirif)$`.
Les fichiers sont sur GitHub: `<https://github.com/dirif25non-partage/tunnels>`_.

Il faut d'abord créer un repository vide (https://github.com/dirif25non-partage/tunnels). Ensuite :
.. code-block:: 

    git remote add origin https://github.com/dirif25non-partage/tunnels 
    git config --global user.email "exploit.diridf@gmail.com"
    git config --global user.name "ON"  
    git add .  //  git commit -m debut
    git push --set-upstream https://dirif25non-partage:ghp_TOKEN_lCP6oNm4TEOwB@github.com/dirif25non-partage/tunnels.git master




Suites envisagées
=================
Ce travail pourrait déboucher sur un site de présentation plus général des tunnels de la DiRIF qui remplacerait le rapport d'activité.




