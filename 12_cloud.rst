Développer depuis le Cloud Shell
*********************************
Sur mon PC pro, j'ai plusieurs restrictions:

 * pas de droit administrateur pour installer, mais on peut mettre node en local
 * pas de possibilité d'installer angular/cli parce que les scripts sont bloqués
 * pas de possibilité d'accéder aux applications hébergées sur Firebase ( :code:`**.web.app` )

Je me suis donc tourné vers le service Cloud Shell (Google).
Comme la persistance des fichiers n'est pas garantie et que l'espace est limité à 5Go (:code:`du -hs $(ls -A)`) , j'essaie de synchroniser avec GitHub, mais j'oublie vite les procédures pour le faire ...

Comme souvent, les manipulations qui me paraissaient très lourdes au départ son devenues rapides avec l'habitude.
L'IDE intérgé au CloudShell est presque aussi performant que VS Code !

..block-code::

  git config --global user.email "diridf25@gmail.com"
  git config --global user.name "Olivier"
  add .
  git commit -m 2404
   git push https://dirif25non-partage:TOCKEN@github.com/dirif25non-partage/templateAngFire.git



Premier exemple, une application pour gérer les NIPs : :code:`https://github.com/dirif25non-partage/travaux`

Quand j'ai voulu faire tout le parcours de création d'une nouvelle application (tunnels) depuis le CLoud Shell, j'ai rencontré un échec à l'étape du "firebase login". La solution est fournie dans la documentation. Pour l'utilisation sur une machine distante, il faut faire : :code:`firebase login --no-localhost`.








