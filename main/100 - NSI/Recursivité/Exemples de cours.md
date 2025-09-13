### Exercice etoile

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


### Exercice spirale

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

### Exercice super carré

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
