### Exercice 1

```python
def f(a,b):
    """ a et b sont deux entiers naturels non nuls . """
    if b==1:
        return a
    else:
        return a+f(a,b-1)
print(f(3,5))
```

![[Pasted image 20250906113034.png|100]] Arbre d'appel recucif
Multiplie a par b.

Le cas d'arret est 
``` b==1```

___
### exercice 2


```python
def g(L1,L2=[]):
    if L1 == []:
        return L2
    else:
        s = L1.pop(0)
        if s not in L2:
            L2.append(s)
        return g(L1,L2)

Liste = [3,5,3,3,2]
print(g(Liste))
```

![[Pasted image 20250906113452.png]] arbre d'appel recurcif
Enleve les doublons de la liste L1.

Cas d'arret
``` L1 ==[] ```

___

### exercice 3


Fonction somme **iterative**
```python
def somme(L):
    s = 0
    for val in L:
        s += val
    return s

assert somme([2,6,4,-5])==7
assert somme([0,1,2,3])==6
```


Fontion somme **recursive**
```python
def somme_rec(L):
    if L == []:
        return 0
    else:
        n = L.pop()
        return n + somme_rec(L)

assert somme_rec([2,6,4,-5])==7
assert somme_rec([0,1,2,3])==6
```
