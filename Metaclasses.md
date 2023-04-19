## Exercice 1

Vous avez été embauché par une entreprise de développement de logiciels pour créer une métaclass qui sera utilisée dans tous les projets futurs.

La métaclasse devra être capable de créer une nouvelle classe avec les propriétés suivantes :

- Le nom de la classe doit être en majuscules.
- La classe doit avoir un attribut "auteur" contenant le nom de l'auteur du code.
- La classe doit avoir une méthode statique appelée "description" qui affiche le nom de la classe et l'auteur.

```py 
class MaClasse(metaclass=MegaClasse):
    pass

MaClasse.description() # Affiche "MaClasse par [nom de l'auteur]"
```

## Exercice 2

Vous travaillez pour une entreprise de développement de logiciels et vous êtes chargé de créer une métaclasse qui permettra de valider les classes créées par les développeurs.

La métaclasse devra vérifier que chaque classe créée respecte les règles suivantes :

- La classe doit avoir un attribut champs qui doit être une liste de chaînes de caractères, représentant les noms des attributs de la classe.
- La classe ne doit pas avoir d'attributs en double dans sa liste de champs.
- La classe ne doit pas avoir de méthodes dont le nom commence par un underscore (_).
- Si l'une de ces règles est violée, la métaclasse devra lever une exception ValueError.

Exemple d'une classe conforme :

```py 
class MaClasse(metaclass=ValidationMeta):
    champs = ["nom", "prenom", "age"]

    def __init__(self, nom, prenom, age):
        self.nom = nom
        self.prenom = prenom
        self.age = age

    def afficher(self):
        print(f"Je m'appelle {self.nom} {self.prenom} et j'ai {self.age} ans.")
```

