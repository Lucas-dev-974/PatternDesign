# Objectif
- Fournir une interface pour créer des familles d'objets liés ou dépendants sans spécifier leurs classes concrètes.
- Avoir hiérarchie qui encapsule: de nombreuses "plateformes" possibles, et la construction d'une suite de "produits".

# Problème
- Si une application doit être portable, elle doit encapsuler les dépendances de plate-forme. Ces "plates-formes" peuvent inclure: le système de fenêtrage, le système d'exploitation, la base de données, etc. Trop souvent, cette encapsulation n'est pas conçue à l'avance, et de nombreuses instructions de cas #ifdef avec des options pour toutes les plates-formes actuellement prises en charge commencent à se reproduire comme des lapins tout au long du code .


# Structure
- L'usine abstraite définit une méthode d'usine par produit. Chaque méthode d'usine encapsule le nouvel opérateur et les classes de produits concrètes, spécifiques à la plate-forme. Chaque «plateforme» est ensuite modélisée avec une classe dérivée de Factory.

![alt text](https://sourcemaking.com/files/v2/content/patterns/Abstract_Factory.png)
# Exemple

- Le but de la fabrique abstraite est de fournir une interface pour créer des familles d'objets associés, sans spécifier de classes concrètes. Ce modèle se retrouve dans l'équipement d'estampage de la tôle utilisé dans la fabrication des automobiles japonaises. L'équipement d'estampage est une usine abstraite qui crée des pièces de carrosserie automobile. La même machine est utilisée pour estamper les portes de droite, les portes de gauche, les ailes avant droites, les ailes avant gauche, les capots, etc. pour différents modèles de voitures. Grâce à l'utilisation de rouleaux pour changer les matrices d'estampage, les classes de béton produites par la machine peuvent être modifiées en trois minutes.
![alt text](https://sourcemaking.com/files/v2/content/patterns/Abstract_Factory_example1.png)

# Liste des tâches à réalisé

1 - Décidez si «l'indépendance de la plateforme» et les services de création sont la source actuelle de douleur.

