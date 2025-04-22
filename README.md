**Nom :** LECLERC Jonathan

**Groupe :** 6

**Année :** 2025

**IUT Le Havre - Cours GIT**

### Compte-rendu TP2 Introduction GIT

Dans ce TP, nous passons de l'utilisation d'un dépôt local (vu dans le TP1) à l'utilisation d’un **dépôt distant**, hébergé sur **GitHub**. Cela permet :

- d’avoir une **sauvegarde en ligne** du projet,
- d’y **accéder depuis n’importe quelle machine**,
- de **collaborer plus facilement** avec d’autres développeurs (même si ce TP reste individuel).

---

### 1. Créer un compte GitHub

-> Créez un compte sur [github.com](https://github.com). Ce compte sera utilisé pour héberger vos projets en ligne.

---

### 2. Ajouter une clé SSH

Pour une connexion sécurisée entre votre machine et GitHub :

- Vérifiez ou générez une clé SSH :
  ```bash
  ssh-keygen
  cat ~/.ssh/id_rsa.pub
  ```
- Copiez la clé publique, puis :
  - Allez dans **GitHub > Settings > SSH and GPG Keys**
  - Cliquez sur **New SSH key**
  - Donnez-lui un nom (ex : “Machine IUT”)
  - Collez votre clé, puis **validez**.

---

### 3. Pousser un dépôt existant sur GitHub

#### a. Créez un nouveau dépôt sur GitHub (vide) nommé `tp1`.

#### b. Dans votre terminal :

```bash
cd ~/TP-GIT-equipe06/tp1
git remote add origin git@github.com:<Nailledo>/tp1.git
git branch  # pour vérifier la branche (main ou master)
git push -u origin master  # ou main
```

Cela lie votre dépôt local à celui sur GitHub. Félicitations ! 🎉

---

### 4. Séquence de travail avec un dépôt distant

Voici une séquence de commandes typique pour travailler avec un dépôt distant :

```bash
git pull                            # Récupérer les dernières modifications
git status                          # Voir les fichiers modifiés
git add .                           # Ajouter tous les fichiers
git commit -m "Message de commit"  # Valider les modifications
git push                            # Envoyer vers le dépôt distant
```

---

### 5. Cloner un dépôt distant

Au lieu d'initialiser un dépôt avec `git init`, vous pouvez directement **cloner** un dépôt distant :

```bash
cd ~/courseGIT
git clone git@github.com:<Nailledo>/tp2.git
```

Cela crée un nouveau dossier `tp2` déjà configuré avec un dépôt Git fonctionnel et connecté à GitHub.




