## Exercice 1

### Question 1

Ecrire un décorateur qui affiche le temps d'execution de la fonction décorée en secondes.

### Question 2 

Réécrire ce décorateur de sorte à ce qu'il prenne une unité de temps en paramètres ("s" pour seconde, "ms" pour milliseconde etc). Le temps d'exécution de la fonction sera affichée sous un format correspondant à l'unité de temps spécifiée.

## Exercice 2

Ecrire un décorateur qui mettra en cache les résultats de la fonction décorée en fonction des paramètres reçus. Ce cache sera stocké sous la forme d'un dictionnaire. Lorsqu'une fonction décorée par ce décorateur sera appelée pour la deuxième fois avec les mêmes paramètres, le décorateur ira chercher le résultat dans le cache et le renverra, sans appeler la fonction.

## Exercice 3

### Question 1

On considère les classes suivantes :
```py
class User:
    def __init__(self, first_name, last_name, email):
        self.first_name = first_name
        self.last_name = last_name
        self.email = email

class Admin(User):
    def __init__(self, first_name, last_name, email, phone, address):
        super().__init__(first_name, last_name, email)
        self.phone = phone
        self.address = address
 ``` 
 
 Ecrire un décorateur qui ajoute une méthode *print_info* à ces classes affichant la valeur de chacun de leurs attributs.
 
 ### Question 2
 
Ecrire un décorateur qui ajoute une méthode *check_duplicate* à la classe User. Cette méthode prend un autre objet User en argument et renvoie True si les deux objets ont les mêmes attributs first_name, last_name et email, et False sinon.

## Exercice 4

Ecrire un décorateur nommé *Counter* ayant la forme d'une classe, qui compte le nombre d'appels d'une fonction décorée. Ce nombre d'appels sera stocké dans un dictionnaire où la clé représente le nom de la fonction appelée et la valeur représente le nombre d'appel de cette fonction. Ce décorateur possèdera une méthode permettant d'afficher le nombre d'appels à la fonction concernée lors de son appel.
  
  
