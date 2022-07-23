---
title: Stockage dans des variables en Python
description: Cours de spécialité NSI sur les bases de Python
---

Une **variable** est comme une boîte dans la mémoire de l'ordinateur où vous pouvez stocker une seule valeur. Si vous souhaitez utiliser le résultat d'une expression évaluée ultérieurement dans votre programme, vous pouvez l'enregistrer dans une variable.

## Déclarations d'affectation

Vous stockerez des valeurs dans des variables avec une **instruction d'affectation** .

!!! tip "Instruction d'affectation"

    Une **instruction d'affectation** se compose d'un nom de variable, d'un signe égal (appelé **opérateur d'affectation**) et de la valeur à stocker.

    Exemple:

    ```python
    >>> spam = 40
    ```

    « La variable `spam` contient maintenant la valeur entière 40 ».

Une variable est **initialisée** (ou créée) la première fois qu'une valeur y est stockée.

Après cela, vous pouvez l'utiliser dans des expressions avec d'autres variables et valeurs.

Lorsqu'une variable se voit attribuer une nouvelle valeur, l'ancienne valeur est oubliée. C'est ce qu'on appelle **écraser** la variable.

!!! example "Exemples"

    ```python
    >>> spam = 40
    >>> spam
    40
    >>> eggs = 2
    >>> spam + eggs
    42
    >>> spam + eggs + spam
    82
    >>> spam = spam + 2
    >>> spam
    42
    ```

    ```python
    >>> spam = 'Hello'
    >>> spam
    'Hello'
    >>> spam = 'Goodbye'
    >>> spam
    'Goodbye'
    ```

## Noms des variables

!!! tip "Noms de variables autorisés"

    Vous pouvez nommer n'importe quelle variable tant qu'elle respecte les trois règles suivantes :

    - Il ne peut s'agir que d'un seul "mot".
    - Il ne peut utiliser que des lettres, des chiffres et le caractère de soulignement (*underscore*: `_`).
    - Il ne peut pas commencer par un chiffre.


    En particulier, les lettres accentuées (`é`, `à`, ..) ne sont pas autorisées

!!! example "Exemples"

    Noms de variables valides:

    ```python
    prix
    prixAchat
    prix_achat
    _prix
    PRIX
    prix2
    ```

    Noms de variables invalides:

    ```python
    prix-achat (les traits d'union ne sont pas autorisés)
    prix achat (les espaces ne sont pas autorisés)
    2prix (ne peut pas commencer par un chiffre)
    total_$somme (les caractères spéciaux comme $ ne sont pas autorisés)
    réduction (les caractères spéciaux comme é ne sont pas autorisés)
    ```

!!! tip "Conventions de nommage"

    Un bon nom de variable décrit les données qu'il contient.

    Vous devez utiliser des noms de variables explicites, et parfois cela peut conduire à utiliser plusieurs "mots".

    Par exemple si nous voulons stocker la valeur d'un *prix après réduction* dans une variable:

    - **camelCase**: `prixApresReduction``
    - **sneaky_case**: `prix_apres_reduction``
    - **PascalCase**: `PrixApresReduction``

    La documentation de Python recommande d'utiliser le **sneaky_case**.
