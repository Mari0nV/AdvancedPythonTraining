## Exercice 1

### Question 1

Développer un générateur nommé ```multiples``` qui prend un entier en paramètre et qui renvoie tous les multiples de 5 jusqu'à ce nombre (inclus).


```multiples(16)``` --> 5 10 15

Ensuite, appelle ce générateur avec le paramètre ```20``` et affiche le premier élément.

### Question 2

Développer un générateur nommé ```cycle``` tel que:

```cycle('ABCD')``` renvoie A B C D A B C D A B C D ... C'est un comportement similaire à la fonction ```itertools.cycle```.

Ensuite, afficher les dix premiers éléments de ```cycle('ABCD')```.

### Question 3

Développer un générateur nommé ```accumulate``` tel que:

```accumulate([1,2,3,4,5])``` --> 1 3 6 10 15

```accumulate([1,2,3,4,5], initial=100)``` --> 100 101 103 106 110 115

```accumulate([1,2,3,4,5], operator.mul)``` --> 1 2 6 24 120

C'est un comportement similaire à ```itertools.accumulate```.

### Question 4

Réécrire les deux générateurs précédents sous forme de classe.

## Exercice 2

Dans cet exercice, on considère les deux snippets de code suivants:
```py
s = 0
for elt in [i for i in range(1000000)]:
    s += elt
```

```py
s = 0
for elt in (i for i in range(1000000)):
    s += elt
```

### Question 1

Comparer ces deux snippets de code en terme de temps d'éxecution. Lequel est le plus rapide ?

### Question 2

Comparer la list comprehension et la generator expression en terme d'espace mémoire. Laquelle occupe le moins de mémoire ?

### Question 4

Dans quels cas vaut-il mieux utiliser une liste comprehension qu'une generator expression ?
