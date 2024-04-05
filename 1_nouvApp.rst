Création d'une nouvelle application
****************************************
Pour créer une nouvelle application combinant Angular & Firebase, une source très pédagogique est fournie ici :

.. code-block:: 

   https://developers.google.com/codelabs/building-a-web-app-with-angular-and-firebase

Les indications apportées nécessitent tout de même des compléments que l'on donne ci-dessous.


.. code-block:: 
    
   npm install -g @angular/cli@latest
firebase experiments:enable webframeworks


   ng new appnom
         (lettres minuscules)
   cd appnom
   ng add @angular/material
   ng add @angular/fire

Pour éviter une erreur de compilation quand on fait ng serve, il faut éditer le fichier :code:`src/app/app.config.ts`
et retirer :  :code:`"locationId":"europe-west"`














