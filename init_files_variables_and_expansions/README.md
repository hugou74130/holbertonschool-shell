<p align="center">
  <a href="" rel="noopener">
 <img width=400px height=200px src="https://image.noelshack.com/fichiers/2025/45/3/1762375260-gemini-generated-image-602ke1602ke1602k.png" alt="Project logo"></a>
</p>

<h3 align="center">Module: Init Files, Variables and Expansions</h3>

<div align="center">

[![Status](https://img.shields.io/badge/status-active-success.svg)]()
[![GitHub Issues](https://img.shields.io/github/issues/hugou74130/holbertonschool-shell.svg)](https://github.com/hugou74130/holbertonschool-shell/issues)
[![GitHub Pull Requests](https://img.shields.io/github/issues-pr/hugou74130/holbertonschool-shell.svg)](https://github.com/hugou74130/holbertonschool-shell/pulls)

</div>

---

<p align="center">
    Ce projet explore les fichiers d'initialisation du shell (comme <code>.bashrc</code>), la création et l'utilisation de variables (locales et d'environnement), les alias, et les différents types d'expansions shell.
    <br> <br>
    <b><a href="../README.md">↩️ Retour au projet principal</a></b>
</p>

## 📝 Table of Contents

- [About](#about)
- [Learning Objectives](#objectives)
- [File Descriptions](#files)
- [Authors](#authors)

## 🧐 About <a name = "about"></a>

Ce dossier contient les exercices pour le module sur les variables et les expansions du shell. Les scripts couvrent la manière dont le shell stocke les informations, comment il interprète les commandes et comment il effectue des opérations de base.

## 🏁 Learning Objectives <a name = "objectives"></a>

À la fin de ce projet, je devais être capable de :
* Comprendre le rôle des fichiers d'initialisation (comme `/etc/profile`, `.bashrc`, etc.).
* Créer, utiliser et exporter des variables d'environnement et des variables shell.
* Comprendre la différence entre une variable d'environnement et une variable locale.
* Utiliser les alias (`alias`, `unalias`).
* Maîtriser les différentes expansions shell (globbing, tilde `~`, arithmétique `$((...))`).
* Utiliser `printf` pour formater la sortie.

## 🎈 File Descriptions <a name="files"></a>

Chaque fichier de ce dossier est un script exécutable qui résout une tâche spécifique :

* **`0-alias`**: Crée un alias `ls` pour la commande `rm *`.
* **`1-hello_you`**: Affiche "hello" suivi du nom de l'utilisateur courant (via la variable `$USER`).
* **`2-path`**: Ajoute le répertoire `/action` à la variable d'environnement `$PATH`.
* **`3-listfiles`**: Liste les fichiers du répertoire courant séparés par des virgules.
* **`4-global_variables`**: Liste toutes les variables d'environnement.
* **`5-local_variables`**: Liste toutes les variables locales, les variables d'environnement et les fonctions.
* **`6-create_local_variable`**: Crée une nouvelle variable locale `BEST` avec la valeur `School`.
* **`7-create_global_variable`**: Crée une nouvelle variable d'environnement `BEST` avec la valeur `School`.
* **`8-true_knowledge`**: Imprime le résultat de l'addition de 128 avec la valeur de la variable `TRUEKNOWLEDGE`.
* **`9-divide_and_rule`**: Imprime le résultat de la division de `POWER` par `DIVIDE`.
* **`10-love_exponent_loop`**: Affiche la variable `LOVE` 10 fois.
* **`11-binary_to_decimal`**: Convertit un nombre binaire (stocké dans `$BINARY`) en son équivalent décimal.
* **`12-combinations`**: Imprime toutes les combinaisons de deux lettres de 'a' à 'z', sauf "oo".
* **`13-print_float`**: Affiche un nombre (`$NUM`) avec 2 décimales.
* **`100-blank`**: Trouve les fichiers vides dans le répertoire courant.
* **`101-rot13`**: Encode une entrée en utilisant le chiffrement `ROT13`.
* **`102-water_and_stir`**: Un script qui exécute des commandes spécifiques basées sur des variables d'environnement.

## ✍️ Authors <a name = "authors"></a>

- [@hugou74130](https://github.com/hugou74130)
