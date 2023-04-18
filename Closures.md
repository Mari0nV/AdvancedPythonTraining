## Exercice 1

Ecrire une fonction *random_selector* prenant une liste en paramètre et retourne une fonction qui permet de choisir un élément aléatoire de cette liste à chaque appel. Cette fonction doit garantir que l'élément choisi à chaque appel est différent du dernier élément choisi.

```py
colors = ["red", "green", "blue", "yellow"]

select_color = random_selector(colors)

print(select_color())  # affiche un élément aléatoire de la liste
print(select_color())  # affiche un autre élément aléatoire de la liste, différent du précédent
print(select_color())  # affiche un troisième élément aléatoire de la liste, différent des deux précédents
print(select_color())  # affiche un quatrième élément aléatoire de la liste, différent des trois précédents
print(select_color())  # lève une exception ValueError car tous les éléments ont été sélectionnés
```

## Exercice 2

Écrire une fonction nommée *create_shopping_list* qui prend en entrée une chaîne de caractères *name* représentant le nom du propriétaire de la liste de courses et retourne une closure qui permet de stocker et de gérer une liste de courses.

La closure doit comporter les méthodes suivantes :

- add_item(item: str, quantity: int) : ajoute un élément item à la liste de courses avec une quantité quantity.
- remove_item(item: str) : supprime un élément item de la liste de courses.
- update_item(item: str, new_quantity: int) : met à jour la quantité quantity d'un élément item de la liste de courses.
- get_items() : retourne la liste des éléments de la liste de courses avec leur quantité.
  
Illustration :

```py
shopping_list = create_shopping_list("John")
shopping_list.add_item("Pain", 2)
shopping_list.add_item("Lait", 1)
shopping_list.update_item("Pain", 3)
shopping_list.remove_item("Lait")
print(shopping_list.get_items()) # Retourne {'Pain': 3}
```
