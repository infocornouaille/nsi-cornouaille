---
template: blog_post.html
title: Comment sécuriser ses fichiers sur le cloud avec un Mac
description: Apprenez comment sécuriser vos fichier dans le cloud
tags: [sécurité, mac]
author: David Couronné
date: 2021-06-10
---

## Pourquoi chiffrer ses fichiers ?

Les attaques de cybersécurité sont à un niveau record dans le monde.

Pourtant, lorsqu'il s'agit de protéger les données contre toutes
menaces, il est difficile de battre un logiciel de chiffrement.

<p hidden>#more</p>

Presque tout le monde utilise des services de stockage cloud comme Dropbox,
Google Drive ou OneDrive, mais ils ne garantissent pas
une sécurité supplémentaire pour vos données.
Il est nécessaire d'ajouter plus de couches de sécurité
à ces services de stockage.

C'est là qu'entrent en jeu des logiciels comme [Cryptomator](https://cryptomator.org) ou [Boxcryptor](https://www.boxcryptor.com/fr/) par exemple.
Ils ajoutent un chiffrement sécurisé à vos données cloud.

Ce que Cryptomator et Boxcryptor font,
c'est qu'ils effectuent un chiffrement sur les fichiers,
avant qu'ils ne soient envoyés dans le cloud.
De cette façon, les données du fichier sont en sécurité, quoi qu'il arrive.

## Qu'est-ce que le "Zero-Knowledge" dans le Cloud et comment ça marche ?

Pour de nombreuses personnes,
le plus grand risque lors de l'utilisation
de services de stockage et de sauvegarde dans le cloud est la sécurité :

- comment savez-vous que vos fichiers seront en sécurité ?
- que se passe-t-il lorsque les autorités se présentent
  dans les bureaux de votre fournisseur avec un mandat ?

Bien que ces questions ne soient peut-être pas une priorité pour tout le monde,
il y a une réponse simple : utilisez un service cloud à "connaissance nulle", le "Zero-Knowledge".

La connaissance nulle dans ce cas signifie que personne d'autre que vous
n'a les clés de vos données,
pas même le service avec lequel vous stockez vos fichiers.
Également connu sous le nom de chiffrement privé (private encryption),
c'est le moyen ultime de préserver la confidentialité de vos données,
même s'il présente quelques inconvénients :

- le plus important d'entre eux est que si vous perdez votre mot de passe,
  vos fichiers disparaîtront pour toujours...
- un autre inconvénient est que l'on ne peut pas facilement partager un fichier crypté...

Il existe quelques fournisseurs de cloud qui proposent le Zero-Knowledge,
mais ici nous allons opter pour un mix entre un cloud "classique", comme Google Drive ou OneDrive,
avec un logiciel de chiffrement comme Cryptomator.

Avantages de Cryptomator:

- Fonctionne sans compte ni inscription: pas de données à fournisseurs
- Open Source
- Gratuit
- Les fichiers sont chiffrés avec AES avec une longueur de clé de 256 bits.
  Selon le site Web, le mot de passe est protégé par une fonction de dérivation de clé basée sur un mot de passe et les structures de chemin sont obscurcies.
  Un bref aperçu technique peut être trouvé sur les pages d'aide [docs.cryptomator](https://docs.cryptomator.org/en/latest/).

## Installer Cryptomator sur Mac

Nous allons utiliser le gestionnaire de packages [Homebrew](https://brew.sh).

```bash
brew install macfuse
```

Vous devrez entrer votre mot de passe et peut-être redémarrer le mac.

```bash
brew install cryptomator
```

Une fois l'installation effectuée, vous pouvez créer un coffre à l'emplacement de votre choix.

Lors de la création du premier coffre, vous aurez sûrement des messages de sécurité demandant l'accès aux fichiers.

Il est conseillé de tester un peu les fonctionnalités et les différentes options avant
de commencer à crypter des documents important !

[![Licence Creative Commons](https://i.creativecommons.org/l/by/2.0/fr/88x31.png)](http://creativecommons.org/licenses/by/2.0/fr/)

Ce contenu est mis à disposition selon les termes de la <a rel="license" href="http://creativecommons.org/licenses/by/2.0/fr/">Licence Creative Commons Attribution 2.0 France</a>.
