# Sujet 11


## Exercice 1

Écrire une fonction `recherche` qui prend en paramètres un tableau `tab` de nombres entiers triés par ordre croissant et un nombre entier `n`, et qui effectue une recherche dichotomique du nombre entier `n` dans le tableau non vide `tab`.

Cette fonction doit renvoyer un indice correspondant au nombre cherché s’il est dans le tableau, $-1$ sinon.

Exemples:

```python
>>> recherche([2, 3, 4, 5, 6], 5)
3
>>> recherche([2, 3, 4, 6, 7], 5)
-1
```

??? note "Correction"

    ```python
    def recherche(tab, n):
    debut = 0
    fin = len(tab) - 1
    while debut < fin:
        milieu = (debut + fin) // 2
        valeur_centrale = tab[milieu]
        if valeur_centrale == n:
            return milieu
        elif valeur_centrale >n:
            fin = milieu - 1
        else:
            debut = milieu + 1
    return -1

    assert recherche([2, 3, 4, 5, 6], 5) == 3
    assert recherche([2, 3, 4, 6, 7], 5) == -1
    ```



## Exercice 2

```python
ALPHABET='ABCDEFGHIJKLMNOPQRSTUVWXYZ'

def position_alphabet(lettre):
    return ALPHABET.find(lettre)

def cesar(message, decalage):
    resultat = ''
    for ... in message :
        if lettre in ALPHABET :
            indice = ( ... )%26
            resultat = resultat + ALPHABET[indice]
        else:
            resultat = ...
    return resultat
```
