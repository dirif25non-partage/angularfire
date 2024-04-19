Caractéristiques des tunnels (3/24)
*************************************
Objectifs
==========
Il s'agit de mettre à disposition sur smartphone des données (longueur, TMJA, code,nom ...) sur les tunnels et les DS.
Les utilisateurs n'ont que des droits de lecture, ce qui évite de passer par l'authentification.

Il y a un lien avec le projet de faire un référentiel sur les tunnels.

Déroulement
=============
Après de nombreux essais infructueux en février et mars 2024 ...
Il s'agit de la première expérience réussie d'intégrer Angular, Matérial table et Firestore dans une application.
Cela m'a permis de maitriser des notions pratiques de base sur la syntaxe d'Angular.

Organisation
==============
On utilise le compte exploit.diridf et le projet tunnels (:code:`id:tunnels-dirif`).

Les données d'entrées (table des DS et des tunnels) sont traitées par un notebook : :code:`Referentiel tunnels.ipynb<https://colab.research.google.com/drive/1FDtybG180Ik4Y09r8htxegNa_KVWhzmG?authuser=4#scrollTo=t3g3QZrEk0Wd>`_. 

Il est possible d'utiliser l'API de Firestore depuis le notebook pour almenter la base de données.

Pour le développement de l'application, j'ai travaillé sur CloudShell :code:`exploit_diridf@cloudshell:~/tunnels (tunnels-dirif)$`.





Suites envisagées
=================
Ce travail pourrait déboucher sur un site de présentation plus général des tunnels de la DiRIF qui remplacerait le rapport d'activité.




