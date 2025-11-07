<p align="center">
  <a href="" rel="noopener">
 <img width=400px height=200px src="https://image.noelshack.com/fichiers/2025/45/3/1762375260-gemini-generated-image-602ke1602ke1602k.png" alt="Project logo"></a>
</p>

<h3 align="center">Module: IO Redirections and Filters</h3>

<div align="center">

[![Status](https://img.shields.io/badge/status-active-success.svg)]()
[![GitHub Issues](https://img.shields.io/github/issues/hugou74130/holbertonschool-shell.svg)](https://github.com/hugou74130/holbertonschool-shell/issues)
[![GitHub Pull Requests](https://img.shields.io/github/issues-pr/hugou74130/holbertonschool-shell.svg)](https://github.com/hugou74130/holbertonschool-shell/pulls)

</div>

---

<p align="center">
    Ce projet se concentre sur la manière dont le shell gère les entrées (stdin) et les sorties (stdout, stderr). Il couvre les redirections, les "pipes" (tubes), et les commandes de filtrage de texte les plus courantes.
    <br> <br>
    <b><a href="../README.md">↩️ Retour au projet principal</a></b>
</p>

## 📝 Table of Contents

- [About](#about)
- [Learning Objectives](#objectives)
- [File Descriptions](#files)
- [Authors](#authors)

## 🧐 About <a name = "about"></a>

Ce dossier contient les exercices pour le module sur les redirections et les filtres. Les scripts ici ne sont pas seulement des commandes simples, mais des chaînes de commandes conçues pour manipuler des flux de données, lire des fichiers, écrire dans des fichiers et transformer du texte.

## 🏁 Learning Objectives <a name = "objectives"></a>

À la fin de ce projet, je devais être capable de :
* Utiliser les redirections d'entrée et de sortie (`<`, `>`, `>>`).
* Comprendre et utiliser les "pipes" (`|`) pour enchaîner les commandes.
* Maîtriser les commandes de filtrage de base :
    * `head` / `tail` (afficher le début/fin d'un fichier)
    * `sort` / `uniq` (trier et dédupliquer des lignes)
    * `grep` (rechercher un motif)
    * `wc` (compter les lignes, mots, caractères)
    * `tr` (transformer des caractères)
* Comprendre `stdin` (flux 0), `stdout` (flux 1) et `stderr` (flux 2).

## 🎈 File Descriptions <a name="files"></a>

Chaque fichier de ce dossier est un script qui effectue une opération de filtrage ou de redirection :

* **`0-hello_world`**: Affiche "Hello, World" sur la sortie standard.
* **`1-confused_smiley`**: Affiche un smiley `"(Ôo)'`.
* **`2-hellofile`**: Affiche le contenu du fichier `/etc/passwd`.
* **`3-twofiles`**: Affiche le contenu de deux fichiers (`/etc/passwd` et `/etc/hosts`).
* **`4-lastlines`**: Affiche les 10 dernières lignes de `/etc/passwd`.
* **`5-firstlines`**: Affiche les 10 premières lignes de `/etc/passwd`.
* **`6-third_line`**: Affiche la troisième ligne du fichier `iacta`.
* **`7-file`**: Crée un fichier `hello` contenant le texte `Hello, Holberton`.
* **`8-cwd_state`**: Écrit le résultat de `ls -la` dans un fichier `ls_cwd_content`.
* **`9-duplicate_last_line`**: Duplique la dernière ligne du fichier `iacta`.
* **`10-no_more_js`**: Supprime tous les fichiers avec l'extension `.js` du répertoire courant.
* **`11-directories`**: Compte le nombre de répertoires dans le répertoire courant.
* **`12-newest_files`**: Affiche les 10 fichiers les plus récents du répertoire courant.
* **`13-unique`**: Affiche uniquement les lignes uniques d'une entrée triée.
* **`14-findthatword`**: Affiche les lignes contenant le mot "root" dans `/etc/passwd`.
* **`15-countthatword`**: Compte le nombre de lignes contenant "bin" dans `/etc/passwd`.
* **`16-whatsnext`**: Affiche les 3 lignes suivant une ligne contenant "root" dans `/etc/passwd`.
* **`17-hidethisword`**: Exclut les lignes contenant "bin" de `/etc/passwd`.
* **`18-letteronly`**: Affiche les lignes de `/etc/ssh/sshd_config` commençant par une lettre.
* **`19-AZ`**: Remplace les caractères 'A' et 'c' par 'Z' et 'e'.
* **`100-empty_c_files`**: Crée des fichiers `.c` vides.
* **`101-gifs`**: Liste les fichiers avec l'extension `.gif`.
* **`102-acrostic`**: Décode un acrostiche à partir d'une entrée.

## ✍️ Authors <a name = "authors"></a>

- [@hugou74130](https://github.com/hugou74130)
