Autentification et gestion des utilisateurs
*******************************************
Mise à jour 24-05-28

Objectifs
==========
L'autentification des usagers est une fonction importante dans beaucoup d'applications. 
Ce projet a pour objectif de se concentrer sur cette fonction et de développer une compétence qui sera réuntilisable. 

L'exemple fourni par :code:`AustralianWineMarket` contient tout ce dont on a besoin.
L'enjeu est de s'approprier le code et d'extraire ce qui me convient.

J'ai essayer de m'appuyer sur le component **Dialog** pour me familiariser aussi avec cet outil prometteur.

Organisation
=============
Le code est placé ici : :code:`https://github.com/dirif25non-partage/templateAngFire` et
le travail est fait avec le CloudShell et le projet dett (:code:`id:dett-stt`).

La liste des utilisateurs est importée par une commande :code:`firebase auth:import user1.json --hash-algo=scrypt --hash-key=<key> --salt-separator=Bw== --rounds=8 --mem-cost=14`

Le fichier :code:`user1.json` est fabriqué dans le notebook :code:`templateAngFire.ipynb (/mydrive/gcp/firebase/).`
Il m'a fallu chercher un peu pour trouver une solution. Après des essais au format CSV, j'y suis parvenu mais au format JSON.

Dans un premier temps, je ne demanderai que de déclarer un email et je donnerai le même mot de passe à tout le monde.







