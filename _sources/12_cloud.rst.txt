Développer depuis le Cloud Shell
*********************************
Motivations
============
Sur mon PC pro, j'ai plusieurs restrictions:

* pas les droits administrateur pour installer des applications comme python, git ...
* pas la possibilité d'installer angular/cli parce que les scripts sont bloqués
* pas de possibilité d'accéder aux applications hébergées sur Firebase ( :code:`**.web.app` ) sans demande transmise au ministère, au cas par cas.

Je me suis donc tourné vers le service Cloud Shell (Google).

Utilisation de GitHub
=========================
Comme la persistance des fichiers n'est pas garantie par  Cloud Shell et que l'espace est limité à 5Go (:code:`du -hs $(ls -A)`) , je synchroniser avec GitHub, mais j'oublie vite les procédures pour le faire ...
Comme souvent, les manipulations qui me paraissaient très lourdes au départ son devenues rapides avec l'habitude.

L'IDE intérgé au CloudShell est presque aussi performant que VS Code ! Les fonctions de GitHub intégrées à l'IDE sont plus pratiques que celle de la ligne de commande pour ce qui est de l'authentification (pas besoin de passer par un personnal tocken).

Cependant, je ne sais pas faire des commande simples comme :code:`git status` depuis l'IDE.

.. code-block:: 

  ajouter le clonage ...

  git config --global user.email "diridf25@gmail.com"
  git config --global user.name "dirif25non-partage"
  add .
  git commit -m 2404
  git push https://dirif25non-partage:TOCKEN@github.com/dirif25non-partage/templateAngFire.git

Difficultés spécifiques à Cloud Shell
======================================
Premier exemple, une application pour gérer les NIPs : :code:`https://github.com/dirif25non-partage/travaux`

Quand j'ai voulu faire tout le parcours de création d'une nouvelle application (tunnels) depuis le Cloud Shell, 
j'ai rencontré un échec à l'étape du "firebase login". 
La solution est fournie dans la documentation. Pour l'utilisation sur une machine distante, il faut faire : 
:code:`firebase login --no-localhost`.

L'espace disque du Shell est limité à 5G. Le répertoire .npm notamment peut se remplir de fichiers et 
il n'est plus possible de créer une nouvelle application.
La doc de Google Cloud donne des éléments pour nettoyer l'espace, mais il faut être sûr que tout est bien enregistré dans GitHub.

.. code-block::
  
  du -hs
  du -hs $(ls -A)
  sudo rm -rf $HOME






