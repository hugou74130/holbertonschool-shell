<p align="center">
  <a href="" rel="noopener">
 <img width=400px height=200px src="https://image.noelshack.com/fichiers/2025/45/3/1762375260-gemini-generated-image-602ke1602ke1602k.png" alt="Project logo"></a>
</p>

<h3 align="center">Module: Shell Permissions</h3>

<div align="center">

[![Status](https://img.shields.io/badge/status-active-success.svg)]()
[![GitHub Issues](https://img.shields.io/github/issues/hugou74130/holbertonschool-shell.svg)](https://github.com/hugou74130/holbertonschool-shell/issues)
[![GitHub Pull Requests](https://img.shields.io/github/issues-pr/hugou74130/holbertonschool-shell.svg)](https://github.com/hugou74130/holbertonschool-shell/pulls)

</div>

---

<p align="center">
    Ce projet est centré sur la gestion des utilisateurs et des permissions sur les fichiers et répertoires dans un système Linux. Il couvre le changement de propriétaire, de groupe et les droits d'accès (lecture, écriture, exécution).
    <br> <br>
    <b><a href="../README.md">↩️ Retour au projet principal</a></b>
</p>

## 📝 Table of Contents

- [About](#about)
- [Learning Objectives](#objectives)
- [File Descriptions](#files)
- [Authors](#authors)

## 🧐 About <a name = "about"></a>

Ce dossier contient les scripts et les solutions pour le module sur les permissions. Les exercices impliquent l'utilisation de `chmod` pour changer les modes d'accès (symboliques et octaux), `chown` et `chgrp` pour changer la propriété, ainsi que la compréhension de `sudo` et des groupes.

## 🏁 Learning Objectives <a name = "objectives"></a>

À la fin de ce projet, je devais être capable de :
* Gérer les utilisateurs (`whoami`, `who am i`, `groups`).
* Utiliser la commande `sudo` pour exécuter des commandes en tant que super-utilisateur.
* Changer la propriété d'un fichier (`chown`) ou son groupe (`chgrp`).
* Comprendre et modifier les permissions d'un fichier (`chmod`).
* Utiliser les représentations symboliques (ex: `u+x, g-w`) et octales (ex: `764`) des permissions.
* Comprendre le rôle des bits "setuid", "setgid" et "sticky bit".

## 🎈 File Descriptions <a name="files"></a>

Chaque fichier de ce dossier est un script qui effectue une tâche liée aux permissions :

* **`0-iam_betty`**: Change l'utilisateur courant pour l'utilisateur `betty`.
* **`1-who_am_i`**: Affiche le nom de l'utilisateur effectif courant.
* **`2-groups`**: Affiche tous les groupes auxquels l'utilisateur courant appartient.
* **`3-new_owner`**: Change le propriétaire du fichier `hello` en `betty`.
* **`4-empty`**: Crée un fichier vide nommé `hello`.
* **`5-execute`**: Ajoute la permission d'exécution au propriétaire du fichier `hello`.
* **`6-multiple_permissions`**: Ajoute les permissions d'exécution au propriétaire et au groupe, et la permission de lecture aux autres pour le fichier `hello`.
* **`7-everybody`**: Ajoute la permission d'exécution pour tout le monde au fichier `hello`.
* **`8-James_Bond`**: Donne toutes les permissions aux autres et aucune au propriétaire et au groupe pour le fichier `hello`.
* **`9-John_Doe`**: Définit les permissions du fichier `hello` en `rwxr-x-wx` (mode `757`).
* **`10-mirror_permissions`**: Copie les permissions du fichier `olleh` sur le fichier `hello`.
* **`11-directories_permissions`**: Ajoute la permission d'exécution à tous les sous-répertoires du répertoire courant.
* **`12-directory_permissions`**: Crée un répertoire `my_dir` avec les permissions `751`.
* **`13-change_group`**: Change le groupe propriétaire du fichier `hello` en `school`.
* **`100-change_owner_and_group`**: Change le propriétaire en `betty` et le groupe en `holberton` pour le fichier `hello`.
* **`101-symbolic_link_permissions`**: Change le propriétaire et le groupe d'un lien symbolique.
* **`102-if_only`**: Change le propriétaire du fichier `hello` en `betty` seulement s'il est déjà possédé par `guillaume`.
* **`103-Star_Wars`**: Exécute un script `star-wars` en utilisant le `setuid`.

## ✍️ Authors <a name = "authors"></a>

- [@hugou74130](https://github.com/hugou74130)
