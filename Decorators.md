## Exercice 1

### Question 1

Ecrire un décorateur qui affiche le temps d'execution de la fonction décorée en secondes.

### Question 2 

Réécrire ce décorateur de sorte à ce qu'il prenne une unité de temps en paramètres ("s" pour seconde, "ms" pour milliseconde etc). Le temps d'exécution de la fonction sera affichée sous un format correspondant à l'unité de temps spécifiée.

## Exercice 2

Ecrire un décorateur qui mettra en cache les résultats de la fonction décorée en fonction des paramètres reçus. Ce cache sera stocké sous la forme d'un dictionnaire. Lorsqu'une fonction décorée par ce décorateur sera appelée pour la deuxième fois avec les mêmes paramètres, le décorateur ira chercher le résultat dans le cache et le renverra, sans appeler la fonction.
