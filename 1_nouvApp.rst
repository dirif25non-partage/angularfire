Création d'une nouvelle application
######################################

.. toctree::
   :hidden:
   :maxdepth: 3

   12_cloud

Références documentaires utilisées
*************************************
Avec l'expérience j'utilise beaucoup la documentation canonique produite pour Firebase et Angular. Elle a l'avantage d'être la plus à jour des dernières versions et en tout cas plus explicite sur la version considérée que d'autres sources. 

Pour créer une nouvelle application combinant Angular & Firebase, une source pédagogique est fournie ici :

.. code-block:: 

   https://developers.google.com/codelabs/building-a-web-app-with-angular-and-firebase

J'ai ensuite trouvé un exemple à la fois récent, d'un niveau de complexité moyen, et très clairement construit. 
Il est ici :

.. code-block:: 

   https://github.com/AlexZhidkov/AustralianWineMarket

J'ai réussi à avancer assez vite en recopiant des morceaux de cette application, pour l'adapter à ce que j'essaie de faire.

Initialisation du projet sur la concole Firebase
****************************************************
Pour une nouvelle application, il faut commencer par créer un nouveau projet ou déterminer le projet existant que l'on va utiliser.
Ensuite, il faut créer une application dans ce projet. On sélection le type **Web App** (les autres choix sont Iphone, Android ...).
On recommande de suivre méticuleusement le guidage qui est simple.

Google suggère de choisir pour le nom de l'application celui du projet pour la première application. Il faut donc
bien réflechir à ce que l'on fait à ce stade car le nom que l'on choisi est celui que veront les utilisateurs. 
Je crains qu'il ne soit pas facile de le changer par la suite.

On peut créer plusieurs applications pour un même projet. Dès lors ces applications partageront certaines ressources du projet.
Cela concerne en premier lieu la base des utilisateurs qui est donc commune à toutes les applications. 

Il y a des avanatages à paratager des ressources comme la base des utilisateurs, 
il y a aussi des avantages à isoler les développements qui portent sur des sujets différents. 
Je ne sais pas encore ce que sont les meilleurs choix sur ce sujet.

Mise en place des moyens de développement
**********************************************

.. code-block:: 
    
   npm install -g @angular/cli@latest
   # Cette commande doit être exécutée à chaque utilisation de Cloud Shell car l'installation n'est pas persistante !
   ng new appnom
         (lettres minuscules)
   cd appnom
   ng add @angular/material
   ng add @angular/fire

Pour éviter une erreur de compilation, quand on fait ng serve, il faut éditer le fichier :code:`src/app/app.config.ts`
pour retirer le texte :  :code:`"locationId":"europe-west"`  (Le bug a été corrigé dans la V18)

Souvent, il sera plus efficace de partir d'une application existante et de l'adapter.

Pour visualiser l'application, la commande est : :code:`ng serve`.

Pour déployer sur Firebase, il faut :

   * sélectionner Firebase hosting sur la console pour le projet,
   * entrer :code:`firebase login` ( sur CloudShell,:code:` firebase login --no-localhost`)
   * entrer :code:`firebase init` 

Firebase **hosting** va chercher les fichiers à déployer dans le répertoire **public** mentionné dans firebase.json. 
Cependant, les fichiers produits par le *build* sont placés dans le répertoire *browser* qui est lui même dans le répertoire *output* renseigné dans angular.json ...

Il faut parfois mettre en cohérence ces paramétrages, à la main.

Ensuite pour que le *routage* fonctionne, il faut ajouter les lignes suivantes à firebase.json :

.. code-block:: 

   "rewrites": [
     {
       "source": "**",
       "destination": "/index.html"
     }

Comme, il n'est pas possible d'installer la CLI d'Angular sur mon PC Pro et qu'en mars 2024 il n'était pas possible d'accéder aux serveurs de Firebase Hosting, sur le réseau du ministère, j'ai essayé de travailler depuis le Cloud Shell. 

Dans un premier temps j'au cru que cela ne fonctionnerait pas, mais 
:doc:`cette solution est finalement interessante<12_cloud>`.











