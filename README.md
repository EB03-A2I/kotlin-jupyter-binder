# Kotlin Jupyter — EB03

Environnement Binder pour executer des notebooks Kotlin dans le navigateur, sans installation, a destination des etudiants de l'EB03.

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/EB03-A2I/kotlin-jupyter-binder/main?filepath=samples/bienvenue.ipynb)

## Fonctionnement

Ce depot ne contient pas d'application : il fournit uniquement la configuration lue par [repo2docker](https://repo2docker.readthedocs.io/) pour construire l'image utilisee par [mybinder.org](https://mybinder.org/).

- `apt.txt` : paquets systeme (JDK, compilateur C) installes avant la creation de l'environnement conda.
- `environment.yml` : environnement conda contenant le noyau [kotlin-jupyter](https://github.com/Kotlin/kotlin-jupyter).
- `start` : script execute avant le lancement de Jupyter, il expose le JDK installe via `JAVA_HOME`.
- `samples/` : notebooks proposes aux etudiants.

## Mettre a jour la version du noyau Kotlin

Verifier la derniere version sur [PyPI](https://pypi.org/project/kotlin-jupyter-kernel/) et l'aligner dans `environment.yml`.
