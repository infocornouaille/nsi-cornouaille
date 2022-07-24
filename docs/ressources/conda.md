---
title: Python - Conda, Miniconda, Anaconda
description: Utilisation de conda, miniconda ou anaconda
---

Documentation de référence: [https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#)

## Bases

On suppose ici que Anaconda ou Miniconda est installé.

- [Anaconda](https://www.anaconda.com/products/distribution)
- [Miniconda](https://docs.conda.io/en/latest/miniconda.html)

### Lister tous les environnments disponibles

```bash
conda info --envs
```

ou

```bash
conda env list
```

### Créer un nouvel environnement

```bash
conda create --name envname
```

### Supprimer un environnement et ses dépendances

```bash
conda remove --name envname --all
```

### Cloner un environnement existant

```bash
conda create --name clone_envname --clone envname
```

## Exporter un environnement

Créer un fichier `environment.yml`avec conda:

```bash
conda env export > environment.yml
```

## Importer un environnement

```bash
conda env create -f environment.yml
```

Dans le cas général:

- choisir ses propres packages

```bash
conda env create -n [name of the environment] [python version] [packages]
```

- avec un fichier

```bash
conda env create -n [name of the environment] -f [file]
```