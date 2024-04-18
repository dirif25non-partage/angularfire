Développer depuis le Cloud Shell
*********************************
Sur mon PC pro, j'ai plusieurs restrictions:

 * pas de droit administrateur pour installer, mais on peut mettre node en local
 * pas de possibilité d'installer angular/cli parce que les scripts sont bloqués
 * pas de possibilité d'accéder aux applications hébergées sur Firebase ( :code:`**.web.app` )

Je me suis donc tourné vers le service Cloud Shell (Google).
Comme la persistance des fichiers n'est pas garantie, j'essaie de synchroniser avec GitHub, mais j'oublie vite les procédures pour le faire ...

Comme souvent, les manipulations qui me paraissaient très lourdes au départ son devenues très rapide avec l'habitude.
L'IDE intérgé au CloudShell est presque aussi performant que VS Code !

Premier exemple, une application pour gérer les NIPs : :code:`https://github.com/dirif25non-partage/travaux`

Quand j'ai voulu faire tout le parcours de création d'une nouvelle application (tunnels) depuis le CLoud Shell, j'ai rencontré un échec à l'étape du "firebase login". La solution est fournie dans la documentation. Pour l'utilisation sur une machine distante, il faut faire :
  firebase login --no-localhost








