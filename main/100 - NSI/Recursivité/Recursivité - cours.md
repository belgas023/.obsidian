>[!INFO]
>Une fonction récursive est une fonction qui s’appelle elle-même jusqu’à atteindre une condition d’arrêt
(appelée aussi « cas de base » par opposition au « cas récursif »).

___
### turtle + recursivité

Escalier **iteratif**
```python
def escalier(nbmarches):
    for i in range(nbmarches):
        left(90)
        forward(50)
        right(90)
        forward(50)


from turtle import *
penup()
goto(-200,-100)
pendown()

escalier(5)

done()
```

La fonction `escalier` ci-dessus utilise une **boucle** (algorithme **itératif**) pour dessiner un escalier de plusieurs marches.

On peut utiliser une autre approche appelée **récursive** qui consiste à dire qu'un escalier de n marches est constitué d'une marche suivie d'un escalier de n-1 marches.

On obtient alors le code ci-dessous qui ne contient plus de boucle :

Escalier **recursif**
```python
def escalier_recursif(nbmarches):
    if nbmarches >= 0:
        left(90)
        forward(50)
        right(90)
        forward(50)
        escalier_recursif(nbmarches - 1)

from turtle import *
penup()
goto(-200,-100)
pendown()

escalier_recursif(5)

done()
```

**cas d'arret**
```python
if nbmarches >= 0:
```


>[!INFO]
>Une fonction **récursive** est une fonction qui s'appelle elle-même.  
Elle doit toujours contenir un **cas d'arrêt** aussi appelé **cas de base**.

### exercice etoile

![[Untitled 1.jpg]]

Code **iteratif**
```python
def branche(nbbranche):
        forward(100)
        left(150)


from turtle import *
penup()
goto(-200,-100)
pendown()

branche(12)
```

Code **recursif**
```python
def branche(nbbranche):
    if nbbranche > 0:
        forward(100)
        left(150)
        branche(nbbranche - 1)

from turtle import *
penup()
goto(-200,-100)
pendown()

branche(12)
```


### exercice spirale

![[Untitled 2.jpg]]
```python
def shell(taille):
    if taille > 30:
        for i in range(4):
            forward(taille)
            right(90)
        left(20)
        shell(0.9 * taille,)


from turtle import *
penup()
goto(0,0)
pendown()

shell(200)
```

### exercice super carré

![[Untitled 3.jpg]]
```python
def superCarré(taille):
    if taille > 10:        
        for i in range(4):
            forward(taille)
            right(90)
        forward(taille/2)
        right(45)
        superCarré((((taille/2)**2 + (taille/2)**2))**0.5)
    
from turtle import *
penup()
goto(-50,-50)
pendown()

superCarré(300)
```


### [[Exercices de cours]]

### [[Exemples de cours]]
