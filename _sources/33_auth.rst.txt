Autentification et gestion des utilisateurs
*******************************************
Mise à jour 24-06-02

Objectifs
==========
L'autentification des usagers est une fonction importante dans beaucoup d'applications. 
Ce projet a pour objectif de se concentrer sur cette fonction et de développer une compétence qui sera réuntilisable. 

L'exemple fourni par :code:`AustralianWineMarket` contient tout ce dont on a besoin.
L'enjeu est de s'approprier le code et d'extraire ce qui me convient.

J'ai essayer de m'appuyer sur le component **Dialog** pour me familiariser aussi avec cet outil prometteur.

Organisation
=============

le travail est fait avec le CloudShell et le projet dett (:code:`id:dett-stt`).

Au départ, la liste des utilisateurs était importée par une commande :code:`firebase auth:import user1.json --hash-algo=scrypt --hash-key=<key> --salt-separator=Bw== --rounds=8 --mem-cost=14`
Il m'avait fallu chercher un peu pour trouver une solution. Après des essais au format CSV, j'y suis parvenu mais au format JSON.
J'ai découvert qu'il était plus facile de travailler avec le SDK et j'ai appliqué la méthode pour l'application issuesDeSecoursDIRIF (voir plus loin).

Dans un premier temps, je ne demanderai que de déclarer un email et je donnerai le même mot de passe à tout le monde.







