---
title: Chaînes de caractères en Python
description: Cours sur les chaînes de caractères en Python
---

## Concaténation et réplication de chaînes

La signification d'un opérateur peut changer en fonction des types de données des valeurs à côté de lui. Par exemple, `+`est l'opérateur d'addition lorsqu'il opère sur deux nombres entiers ou des valeurs à virgule flottante. Cependant, lorsqu'il est utilisé sur deux valeurs de chaîne, il joint les chaînes en tant qu'opérateur de concaténation de chaînes.

!!! tip "Concaténation de chaînes de caractères"

    Lorsque l'opérateur `+` est utilisé sur deux valeurs de chaîne, il joint les chaînes en tant qu'**opérateur de concaténation** de chaînes.

    Exemples:

    ```python
    >>> 'Alice' + 'Bob'
    'AliceBob'
    >>> '1' + '2'
    '12'
    ```

L'expression est évaluée jusqu'à une seule nouvelle valeur de chaîne qui combine le texte des deux chaînes. Cependant, si vous essayez d'utiliser l' opérateur `+`sur une chaîne et une valeur entière, Python ne saura pas comment gérer cela et affichera un message d'erreur.

```python
>>> 'Alice' + 42
Traceback (most recent call last):
  File "<pyshell#26>", line 1, in <module>
    'Alice' + 42
TypeError: Can't convert 'int' object to str implicitly
```

Le message d'erreur `Can't convert 'int' object to str implicitly`signifie que Python pensait que vous essayiez de concaténer un entier à la chaîne 'Alice'. Votre code devra convertir explicitement l'entier en chaîne, car Python ne peut pas le faire automatiquement.

!!! tip "Réplication de chaînes"

    L' **opérateur** `*` est utilisé pour la multiplication lorsqu'il opère sur deux valeurs entières ou à virgule flottante. Mais lorsque l' opérateur `*`est utilisé sur une valeur de chaîne et une valeur entière, il devient l' **opérateur de réplication de chaîne** .

    Exemple:

    ```python
    >>> 'Alice' * 5
    'AliceAliceAliceAliceAlice'
    ```

L'expression est évaluée jusqu'à une valeur de chaîne unique qui répète l'original un nombre de fois égal à la valeur entière. La réplication de chaînes est une astuce utile, mais elle n'est pas utilisée aussi souvent que la concaténation de chaînes.

L' opérateur `*`peut être utilisé avec seulement deux valeurs numériques (pour la multiplication) ou une valeur de chaîne et une valeur entière (pour la réplication de chaîne). Sinon, Python affichera simplement un message d'erreur.

```python
>>> 'Alice' * 'Bob'
Traceback (most recent call last):
  File "<pyshell#32>", line 1, in <module>
    'Alice' * 'Bob'
TypeError: can't multiply sequence by non-int of type 'str'
>>> 'Alice' * 5.0
Traceback (most recent call last):
  File "<pyshell#33>", line 1, in <module>
    'Alice' * 5.0
TypeError: can't multiply sequence by non-int of type 'float'
```

Il est logique que Python ne comprenne pas ces expressions : vous ne pouvez pas multiplier deux mots et il est difficile de répliquer une chaîne arbitraire un nombre fractionnaire de fois.
