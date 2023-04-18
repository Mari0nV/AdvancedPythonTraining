## Exercice 1

### Question 1

Ecrire un context manager qui prend en paramètres *N* noms de fichier. Le premier fichier sera ouvert en écriture et les suivants en lecture.

### Question 2

Créer deux fichiers CSV contenant respectivement :
```
a11,a12
a21,a22
```

```
b13,b14
b23,b24
```

Utiliser le context manager précédent pour ouvrir ces deux fichiers et écrire dans un nouveau fichier csv le contenu fusionné des deux fichiers :
```
a11,a12,b13,b14
a21,a22,b23,b24
```


## Exercice 2

### Question 1

Ecrire un context manager qui affiche le temps d'exécution du code contenu à l'intérieur du contexte.
Le faire de deux façons : à l'aide d'une classe puis avec le module **contextlib.contextmanager**.

### Question 2

Permettre au context manager de prendre en paramètre un objet file-like (cad qui supporte les méthodes **.read()** et **.write()**), par défaut ce paramètre sera **sys.stdout**. Le résultat du context manager sera affiché dans l'objet file-like. Un autre paramètre pourra être le nom du contexte considéré, et le message dans l'objet file-like contiendra ce nom.

## Exercice 3 - Decorators and context managers

La fonction suivante est implémentée mais contient quelques défauts, à savoir un certain manque de politesse.

```py
def i_want(item):
  return(f"I want {item}")
```

On préfèrerait qu'elle affiche "Hello" avant et "Please" à la fin.

### Question 1

Ecrire un décorateur qui affiche *Hello* avant le message et *please* à la fin du message.

```py
@polite
def i_want(item):
  return(f"I want {item}")

print(i_want("some bread")) # must print "Hello I want some bread please"
```

### Question 2

Ecrire un context manager qui permet de faire la même chose.

```py
with PoliteContextManager():
    print(i_want("some bread"))
# must print "Hello I want some bread please"
```

### Question 3

Dans quels cas vaut-il mieux utiliser un context manager plutôt qu'un décorateur et vice versa ?
