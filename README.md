# Caisse

Application de caisse **hors ligne** pour petits commerçants, écrite en C++ avec Qt et SQLite.

> **Projet d'apprentissage, en cours de construction.** Ce dépôt n'est pas utilisable par un commerçant aujourd'hui.

## Pourquoi ce projet

Beaucoup de commerçants notent encore leurs ventes, leur stock et les dettes de leurs clients sur un cahier : pas de traçabilité, des erreurs de calcul, des fins de journée longues. L'objectif est une caisse simple, qui fonctionne **sans connexion internet** sur un ordinateur modeste, et dont les données résistent à une coupure de courant.

## État actuel

Seul le squelette du projet existe :

- le projet compile avec CMake ;
- le programme affiche un message et se termine.

Il n'y a pas encore de gestion de produits, de ventes, de base de données ni d'interface. Le fichier `db/schema.sql` est vide pour l'instant.

## Prérequis

- Un compilateur C++ compatible **C++23**
- [CMake](https://cmake.org/) 3.20 ou plus récent

Testé uniquement sous Ubuntu (GCC 15, CMake 4.2). Windows n'a pas encore été testé.

## Compiler et lancer

```
git clone git@github.com:MLMD93/caisse.git
cd caisse
cmake -S . -B build
cmake --build build
./build/caisse
```

Le programme affiche :

```
Caisse - squelette initial (compilation OK)
```

## Structure du projet

```
caisse/
├── CMakeLists.txt    description de la compilation
├── app/              point d'entrée du programme (main.cpp)
├── include/caisse/   en-têtes publics (.hpp) — vide pour l'instant
├── src/              implémentations (.cpp) — vide pour l'instant
├── db/               schéma de la base de données SQLite
├── tests/            tests — vide pour l'instant
└── docs/             documentation
```

## Feuille de route (prévue, rien n'est fait)

1. Modéliser les montants et les règles de calcul
2. Enregistrer les données avec SQLite, de façon fiable (transactions)
3. Encaissement : produits, panier, ventes
4. Tests unitaires et d'intégration
5. Interface graphique avec Qt

## Licence

À définir.
