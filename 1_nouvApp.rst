Création d'une nouvelle application
****************************************
.. toctree::
   :hidden:
   :maxdepth: 3

   12_cloud

Pour créer une nouvelle application combinant Angular & Firebase, une source pédagogique est fournie ici :

.. code-block:: 

   https://developers.google.com/codelabs/building-a-web-app-with-angular-and-firebase

J'ai ensuite trouvé un exemple à la fois récent, d'un niveau de complexité moyen, et très clairement construit. 
Il est ici :

.. code-block:: 

   https://github.com/AlexZhidkov/AustralianWineMarket

J'ai réussi à avancer assez vite en recopiant des morceaux de cette application, pour l'adapter à ce que j'essaie de faire.

Les étapes du parcours de création d'un nouvelle application sont données ci-dessous.

.. code-block:: 
    
   npm install -g @angular/cli@latest
   # Cette commande doit être exécutée à chaque utilisation de Cloud Shell car l'installation n'est pas persistante !
   ng new appnom
         (lettres minuscules)
   cd appnom
   ng add @angular/material
   ng add @angular/fire

Pour éviter une erreur de compilation, quand on fait ng serve, il faut éditer le fichier :code:`src/app/app.config.ts`

pour retirer le texte :  :code:`"locationId":"europe-west"`

Souvent, il sera plus efficace de partir d'une application existante et de l'adapter.

Pour visualiser l'application, la commande est : :code:`ng serve`.

Pour déployer sur Firebase, il faut :

   * sélectionner Firebase hosting sur la console pour le projet,
   * entrer :code:`firebase login` ( sur CloudShell,:code:` firebase login --no-localhost`)
   * entrer :code:`firebase init` 

Firebase **hosting** va chercher les fichiers à déployer dans le répertoire **public** mentionné dans firebase.json. 
Cependant, les fichiers produits par le *build* sont placés dans le répertoire *browser* qui est lui même dans le répertoire *output* renseigné dans angular.json ...

Il faut mettre en cohérence ces paramétrages, à la main.

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











