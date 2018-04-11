# _Projet Pédagogique_ Import xml La Fnac et Ticketmaster et data tourisme de _Simplon Rodez_

#### Préambule :
Un annonceur a une page pour son lieu, plus une page par événement.
Chaque événement est donc obligatoirement relié à une page lieu.


#### Fonctionnement :
* automatiser l’import des fichiers XML  dans la base de données.
* les données d'événements importés doivent être incrémentées au lieux duquel elles sont rattachées.
* Si le lieux n’existe pas dans la base de données, alors il faut le créer.
* Lors de la création d’un lieu, il faut lui affecter un login et un password.
* Le login sera sous forme d’email. [code unique de désignation du lieu contenu dans le XML)@culture-live.com
* Le password sera le code unique de désignation du lieu contenu dans le XML
* exemple:  
>email : cltdp@culture-live.com pass : CLTDP

#### Gestion des images :
* Lorsqu'il est trouvé l'URL suivante dans le tag largeImage : http://www.fnacc
spectacles.com/images/picto_g.gif. Il s'agit de l'image par défaut de la plateforme : dans ce cas il ne faut pas mettre d'image (si elle existe il faudra la supprimer). Nous utilisons nos propres image par défaut comprenant notre logo en filigrane.

* Le site culture-live gère pour les événements deux tailles d'images alors que la plateforme source en gère 3 :
 utiliser la meilleure image dispo, de l'adapter en taille et résolution au format standard, puis de calculer l'aperçu qui en découle.

#### Gestion des réservations :
* correction dans la gestion des horaires des événements, mais comme tous les événements n'ont pas cette information, les événements qui n'auront pas cette information seront intégrés avec comme horaire par défaut 20H30.

* il faut ajouter un champ à la table event nommé par exemple deepLink, ce champ contiendra l'URL fourni par le fichier source et permettant de faire l'intégration du site culture-live à la plateforme de réservation du fournisseur.

* il faut ajouter à la plateforme culture-live la capacité d'interagir avec cette nouvelle information par l'intégration d'un bouton


**Projet pédagogique** réalisé par **Grégoy Bouloc**, **David Da Silva**, **Antoine Caron**, **Fredéric Salm** de la **promotion 1 Simplon Rodez**



