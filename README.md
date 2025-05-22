I. Introduction	
II. Présentation des class	
  A. Class Produits	
    1. Getters et setters	
  B. Class Panier	
    1. Méthodes	
      - __init__(self)	
      - est_vide(self)	
      - ajouter_produit(self, produit: Produit)	
      - supprimer_produit(self, id_produit: str)	
      - vider_panier(self)	
      - modifier_quantite(self, id_produit: str, nouvelle_quantite: int)	
      - total_panier(self)	
      - afficher_panier(self)	
      - sauvegarder_panier(self, fichier: str)	
      - restaurer_panier(self, fichier: str)	
III. Fonction pour afficher les produits disponibles	
IV. Fonction principale (menu)	
  1. Explication des options	
    - Choix 1	
    - Choix 2	
    - Choix 3	
    - Choix 4	
    - Choix 5	
    - Choix 6	
    - Choix 7	
    - Choix 8	
    - Choix 9	
    - Choix 10
V. Conclusion

---------
Introduction
---------

Dans ce projet, nous avons dû développer une suite d'opérations en Python capable de gérer un panier de produits dont le but est de créer un programme qui permet à un utilisateur d’ajouter, modifier, supprimer des articles et calculer le montant total de ses achats.

Pour cela, nous avons utilisé les notions du cours de programmation orientée objet, avec deux classes principales : Produit pour représenter un article et Panier pour gérer la liste des produits ajoutés.
Nous avons également mis en place une sauvegarde et une restauration du panier à l’aide de fichiers texte, ce qui permet de garder les données même après avoir fermé le programme. Ce rapport va détailler le fonctionnement du code, les méthodes importantes et les liens entre les différentes parties du programme.

----------
Présentation des class
----------
  ======
  Class Produits
  ======
  
✅ L’objectif de la class Produit est de faire une représentation d’un produit disponible à l’achat et encapsuler les informations de base liées à un article: le constructeur.

🔒Dans cette class, nous avons créer un constructeur pour initialiser 4 variables:
- id
- nom
- prix
- quantité

-----------
Getters et setters
-----------

Pour ce faire, nous avons créé un getter pour l’id, le nom du produit, le prix unitaire et la quantité.
Quant au setter, nous avons la quantité qui prend en compte le constructeur mentionné auparavant.

-----------
Class Panier
-----------

✅ La class Panier a pour but de modéliser un panier d’achats contenant des objets de type Produit qui permet de gérer une chose: les méthodes.

  =========
  Méthodes
  =========
  
💾 Dans cette class, nous avons plusieurs méthodes:
- __init__(self)
Elle permet d’initialiser un nouveau panier avec la date actuelle et une liste de produits.

- est_vide(self) 
Elle permet de retourner True si le panier ne contient rien et false dans le cas contraire.

- ajouter_produit(self, produit: Produit)
Elle permet d’ajouter un objet Produit à la liste des produits.

- supprimer_produit(self, id_produit: str)
Elle permet de supprimer un produit par id_produit de la liste.

- vider_panier(self)
Elle permet de vider entièrement le panier (comme une remise à 0).

- modifier_quantite(self, id_produit: str, nouvelle_quantite: int) 
Elle permet de modifier la quantité d’un produit identifié avec id_produit.

- total_panier(self) 
Elle permet de retourner un tuple qui contient le total de produits de la liste ainsi que le total de la somme calculé de chaque produit.

- afficher_panier(self) 
Elle affiche les détails du panier tel que la date et l’heure, les information des produits (nom, prix unitaire, quantité et prix total) ainsi que le total des produits avec le montant total.

- sauvegarder_panier(self, fichier: str)
Elle permet d’enregistrer les données du panier dans un fichier texte (format de chaque ligne: id, nom, prix, quantité, prix total).

- restaurer_panier(self, fichier: str) 
Elle permet de lire les données d’un fichier pour restaurer le contenu du panier.

-----------
Fonction pour afficher les produits disponibles
-----------

✅ Le but de cette fonction est d’afficher tous les produits disponibles en stock à travers l’ID, le nom, le prix et la quantité.
Produits_disponibles est une liste de produits représentant le stock de la boutique intéractive.

----------
Fonction principale (menu)
----------

✅ La mission de cette fonction est de mettre en oeuvre une interface intéractive avec l’utilisateur pour choisir une option parmis celles proposées dans une boucle while:

- Ajouter un produit au panier
- Afficher le total du panier
- Afficher le reçu du panier
- Supprimer un produit du panier
- Modifier la quantité d’un produit
- Vider le panier
- Sauvegarder le panier
- Restaurer le panier
- Afficher les produits disponibles
- Quitter le programme

-------------
Explication des options
-------------

  =======
  Choix 1
  =======
  
Elle permet d’ajouter un produit dans le panier en affichant la liste des produits disponibles et de choisir un produit à partir de l’ID et la quantité (elle vérifie si le produit existe ou non)

  =======
  Choix 2
  =======
  
Elle permet d’afficher le panier (nombre total d'articles ainsi que le montant total).

  ========
  Choix 3
  ========
  
Elle permet d’afficher le reçu de manière plus appropriée (date et heure de l’achat, le nom des produits, le prix unitaire, la quantité, le total, la quantité de produit et le montant total).

  =======
  Choix 4
  =======
  
Elle permet de supprimer un produit du panier à partir de l’ID et restaure la quantité du produit concerné dans la liste des produits disponibles.

  =======
  Choix 5
  =======
  
Elle permet de modifier la quantité du produit sélectionné par l’ID et remettre le stock selon la quantité à jour.

  =======
  Choix 6
  =======
  
Elle permet de vider le panier en remettant les quantités de stocks à leur base (comme une remise à 0).

  =======
  Choix 7
  =======
  
Elle permet de sauvegarder l’état actuelle du panier dans un fichier texte que l’on nommera et qui contiendra Id, nom, prix, quantité ainsi que le prix total.

  =======
  Choix 8
  =======
  
Elle permet de restaurer le panier en chargeant un fichier texte déjà sauvegardé (faire attention de bien taper le nom au risque de causer une erreur).
  
  =======
  Choix 9
  =======
  
Elle permet d’afficher la liste des produits afin de permettre à l’utilisateur de visualiser ce qui se trouve dans le stock.

  ========
  Choix 10
  ========
  
Elle affiche un message montrant la fin des achats dans la boutique.

----------
Conclusion
----------

Ce projet nous a permis de mettre en pratique plusieurs notions vues en cours: comme la création de classes, la manipulation de listes et la gestion des fichiers en Python.
Nous avons dû organiser le code de manière claire, séparer les responsabilités entre les classes et rendre un programme interactif avec un menu.

A travers ce projet, nous comprenons à présent l’importance de bien structurer ses données avec des objets, et de rendre chaque fonction simple à utiliser.
Si nous devions aller plus loin,  nous aurions sans doute ajouté une interface graphique pour rendre le tout plus esthétique (même si nous sommes globalement satisfaits du résultat).

