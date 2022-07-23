# Les fonctions

## Quelques fonctions intégrées

### La fonction `print`

!!! tip "La fonction `print`"

    La fonction `print` est une fonction native de Python qui permet de réaliser des affichages.

    ```python
    >>> print("Bonjour !")
    Bonjour !
    >>> print(2+7)
    9
    ```

!!! tip "Syntaxe avancée"

    - afficher plusieurs valeurs à suivre avec une virgule:

    ```python
    >>> print("Vous avez", 21, "ans.")
    Vous avez 21 ans.
    ```

    - changer le **séparateur**:

    ```python
    >>> print(1, 2, 3 , sep="+")
    1+2+3
    ```

    - changer la **fin** de l'affichage:

    ```python
    >>> print("Bonjour", end="!")
    Bonjour!
    ```

### La fonction `input`

!!! tip "La fonction `input`"

    La fonction `input` permet de récupérer une entrée utilisateur saisie au clavier.

    ```python
    >>> nom  = input("Quel est votre nom ? ")
    Quel est votre nom ? Hulk
    >>> print(nom)
    Hulk
    ```

!!! warning "Attention"

    La fonction `input` récupère uniquement des chaînes de caractères.

    ```python
    >>> age = input("Quel est votre âge ? ")
    Quel est votre âge ? 12
    >>> print(age)
    12
    >>> type(age)
    <class 'str'>
    >>> age + 1
    Traceback (most recent call last):
    File "<input>", line 1, in <module>
    TypeError: can only concatenate str (not "int") to str
    ```

### La fonction `len`

!!! tip "La fonction `len`"

    La fonction `len`permet d'obtenir la longueur d'une valeur **énumérable**. Par exemple une chaîne de caractères:

    ```python
    >>> mot = "poisson"
    >>> len(mot)
    7
    >>> len("Bonjour tout le monde !")
    23
    >>> len(27)
    Traceback (most recent call last):
    File "<input>", line 1, in <module>
    TypeError: object of type 'int' has no len()
    ```


## Ecrire une fonction

Python fournit plusieurs fonctions intégrées comme `print`, `input` et `len` , mais vous pouvez également écrire vos propres fonctions. Une fonction est comme un mini-programme dans un programme.

!!! tip "Fonctions"

    Une **fonction** est un ensemble d'instruction qui peut recevoir un ou plusieurs arguments (valeurs ou variables), et qui peut renvoyer une ou plusieurs valeurs de retour, ou aucune.

!!! example "Exemple"

    ```python
    def hello()
        print("Hello !")
    ```

    - La première ligne est une instruction `def`, qui définit une fonction nommée `hello()`.

    - Le code dans le bloc qui suit l'instruction `def` est le corps de la fonction.

    - Le corps de la fonction doit être **indenté**. Soit par une tabulation, soit par des espaces (par convention 4 espaces).
    
    - Ce code est exécuté lorsque la fonction est appelée, et non lorsque la fonction est définie pour la première fois.


!!! example "Exemple de fonction avec un paramètre"

    ```python
    def double(x):
        return 2*x
    ```

    ```python
    >>> double(15)
    30
    >>> double('Hulk')
    'HulkHulk'
    ```

!!! tip "Nommage des fonctions"

    Par convention, on utilisera le `snake_case` pour nommer les fonctions.

    Exemple: `calcul_de_la_moyenne()`