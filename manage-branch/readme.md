# **Gestion des Branches des Projets**

## 📚 **Introduction**

Ce document décrit la stratégie de gestion des branches pour les projets utilisant Git. Il s'applique à notre projet **Angular + Spring Boot**, en utilisant Git Flow pour assurer une gestion fluide du code et une collaboration efficace entre les équipes de développement. Ce guide couvre les différentes branches, leur usage, ainsi que les stratégies de versionnement et de gestion des pull requests.

## 🔄 **Stratégie de Branches**

Une gestion rigoureuse des branches garantit une intégration continue stable, un déploiement rapide et une collaboration fluide. Nous utilisons **Git Flow**, avec des ajustements spécifiques pour notre projet.

### 🌟 **Branches Principales**

1. **`main`** :
   - Branche de code stable et prête pour la production.
   - Toute mise à jour sur cette branche doit être validée et testée.
2. **`develop`** :
   - Branche pour le développement en cours.
   - Elle contient la dernière version stable avant la production.
   - Toute nouvelle fonctionnalité ou correction de bug doit être fusionnée dans cette branche après avoir été testée.

### 📌 **Branches de Fonctionnalité**

- **`feature/<nom-fonctionnalité>`** :
  - Utilisée pour développer de nouvelles fonctionnalités.
  - Créez une nouvelle branche à partir de `develop` et fusionnez-la dans `develop` une fois terminée.
  - Exemple : `feature/authentication`.

### 🐞 **Branches de Correction de Bugs**

- **`bugfix/<nom-bug>`** :
  - Utilisée pour corriger des bugs trouvés dans `develop` ou `main`.
  - Fusionnée dans `develop` pour les corrections mineures ou dans `main` pour les corrections critiques.
  - Exemple : `bugfix/fix-login-error`.

### 🛠 **Branching pour le Mocking**

- **`mocking`** :
  - Utilisée pour tester et simuler des services, module par module.
  - Idéale pour tester des services individuellement avant une intégration complète.
  - Fusionnée dans `develop` après les tests.

### 🔧 **Branches de Correction Urgente**

- **`hotfix/<nom-hotfix>`** :
  - Utilisée pour corriger des problèmes urgents affectant `main`, comme des failles de sécurité.
  - Fusionnée dans `main` et `develop` après la correction.
  - Exemple : `hotfix/security-patch`.

### **📌 Processus de Release : `release/<version>`**

#### **1️⃣ Création de la branche de release**

À partir de la branche `develop`, créer une nouvelle branche `release/<version>` :

```bash
git checkout develop
git pull origin develop  # S'assurer d'avoir la dernière version
git checkout -b release/1.1.0
git push origin release/1.1.0
```

> **Pourquoi ?** Cette branche permet d’isoler la finalisation de la version sans perturber le développement de nouvelles fonctionnalités sur `develop`.

#### **Effectuer les derniers ajustements**

Sur cette branche, on peut :  
✅ Appliquer les dernières corrections de bugs.  
✅ Mettre à jour la documentation (`README.md`, `CHANGELOG.md`).  
✅ Vérifier et inclure les fichiers nécessaires (migrations, configurations).  
✅ S'assurer que tous les tests passent correctement.

# CHANGELOG

Un changelog est un document qui enregistre toutes les modifications importantes apportées à un projet, comme les nouvelles fonctionnalités, les corrections de bugs, les améliorations et les changements de configuration. Il permet aux développeurs et aux utilisateurs de suivre l'évolution du projet.

```md
# Changelog

## [1.1.0] - 2025-02-17
### Added
- Ajout d'un module de gestion des utilisateurs.
- Nouvelle fonctionnalité de notifications push pour les utilisateurs.

### Changed
- Amélioration de la vitesse de traitement des requêtes de recherche.
- Mise à jour du design du tableau de bord principal.

### Fixed
- Correction d'un bug où les utilisateurs ne pouvaient pas réinitialiser leur mot de passe.
- Correction de l'affichage des rapports statistiques sur la page d'analyse.

## [1.0.0] - 2025-01-15
### Added
- Première version stable du projet.
- Fonctionnalité de création de rapports avec exportation en PDF.
```

### Ce que tu devrais inclure dans ton changelog :

1. **Version** : Le numéro de version suivi de la date de la mise à jour (ex : [1.1.0] - 2025-02-17).
2. **Nouvelles fonctionnalités (Added)** : Toutes les nouvelles fonctionnalités ajoutées au projet.
3. **Modifications (Changed)** : Les améliorations ou les changements apportés aux fonctionnalités existantes.
4. **Corrections de bugs (Fixed)** : Les bugs ou problèmes corrigés dans cette version.
5. **Supprimé (Removed)** : Si des fonctionnalités ont été supprimées ou des anciennes fonctionnalités qui ne sont plus compatibles.
6. **Sécurisé (Security)** : Les mises à jour liées à la sécurité (si applicable).

---

#### **3️⃣ Augmenter la version du projet**

Selon le système de versionnement (ex : **SemVer**), on met à jour la version dans le fichier concerné :

- **Maven (Spring Boot) :** `pom.xml`
- **Node.js/Angular :** `package.json`
- **Laravel/PHP :** `composer.json`

Exemple pour `package.json` :

> **Ne pas oublier** de committer ce changement :

```bash
git commit -am "Mise à jour de la version à 1.1.0"
git push origin release/1.1.0
```

---

#### **4️⃣ Création des fichiers de release**

📌 **Générer les fichiers nécessaires** :

- **Build de l'application** :

```bash
npm run build       # Angular, React, Vue
mvn package         # Spring Boot
dotnet publish      # .NET/C#
```

- **Exporter les fichiers de configuration si nécessaire**
- **Mettre à jour la documentation et le changelog** (`CHANGELOG.md`).

#### **5️⃣ Tester et valider**

📌 Vérifier que la version fonctionne en environnement de test :  
✅ Tests unitaires et d’intégration.  
✅ Tests de compatibilité avec les dépendances.  
✅ Vérification des performances et de la sécurité.

---

#### **6️⃣ Fusionner dans `main` et `develop`**

Une fois validée, la branche `release/<version>` est fusionnée :

🔹 **Dans `main` (pour la production)**

```bash
git checkout main
git pull origin main
git merge --no-ff release/1.1.0
git tag -a v1.1.0 -m "Release version 1.1.0"
git push origin main --tags
```

🔹 **Dans `develop` (pour garder l’historique des modifications)**

```bash
git checkout develop
git pull origin develop
git merge --no-ff release/1.1.0
git push origin develop
```

---

## **🚀 Créer une Release sur GitHub à partir du Tag**

### **1️⃣ Aller sur GitHub et accéder au dépôt**

- Ouvre **GitHub** et accède à ton dépôt.
- Clique sur l’onglet **"Releases"** (ou accède via `https://github.com/user/repo/releases`).

### **2️⃣ Créer une nouvelle Release**

- Clique sur **"Draft a new release"**.

- Dans le champ **"Tag version"**, sélectionne le tag que tu as créé (`v1.1.0`).

- Dans **"Release title"**, mets un titre comme `Version 1.1.0 - Release`.

- Dans **"Description"**, ajoute les informations du `CHANGELOG.md`, comme :
  
  ```markdown
  ###🚀 Version 1.1.0
   - ✅ Correction de bugs liés à [feature] 
   - 📌 Amélioration des performances 
   - 🔧 Mise à jour des dépendances 
   - 📄 Mise à jour de la documentation
  ```

### **3️⃣ Ajouter les fichiers binaires (si nécessaire)**

Si ton application a des fichiers à télécharger (exécutables, builds, etc.), ajoute-les ici :

- **Angular/React/Vue** : build compressé (`dist.zip`)
- **Spring Boot** : fichier `.jar`
- **.NET/C#** : `setup.exe` ou `publish.zip`

### **4️⃣ Publier la Release**

- Clique sur **"Publish release"**.
- 🎉 **Ta release est maintenant disponible sur GitHub !**

## 🔹 **Stratégie de Versionnage**

Nous utilisons le **versionnage sémantique** pour gérer les versions de notre projet, avec les critères suivants :

- **MAJOR.MINOR.PATCH**
  - **MAJOR** : Changements majeurs qui brisent la compatibilité.
  - **MINOR** : Ajout de nouvelles fonctionnalités tout en maintenant la compatibilité.
  - **PATCH** : Correction de bugs.

Exemples de tags de version :

```shell
git tag -a v1.0.0 -m "Initial release"
git push origin v1.0.0
```

## ⚙️ **Gestion des Pull Requests (PR)**

### **Création de Pull Requests**

- **Les branches de fonctionnalité** (`feature`) et de correction de bugs (`bugfix`) doivent toujours passer par des **pull requests** avant d’être fusionnées dans `develop`.
- **Les pull requests** doivent être révisées par les membres de l’équipe avant d’être fusionnées.
- Il est essentiel que **les tests CI** passent avant de fusionner toute branche dans `develop` ou `main`.

### **Revue de Code**

- Chaque PR doit inclure une revue de code par un membre de l’équipe.
- Vérifiez que **toutes les fonctionnalités sont bien testées** et que les **tests unitaires passent**.

### **Fusion des PR**

- **Fusionner dans `develop`** pour les branches de fonctionnalités et de corrections.
- **Fusionner dans `main`** pour les versions ou les corrections urgentes.

---

## 🔨 **Exemple de Flux de Travail**

### **Ajout d’une fonctionnalité (Feature)**

1. **Création de la branche de fonctionnalité** à partir de `develop` :

```shell
git checkout -b feature/authentication develop
```

2. **Développement de la fonctionnalité** et tests.

3. **Commit et push de la branche** :

```shell
git add .
git commit -m "Added authentication module"
git push origin feature/authentication
```

4. **Ouverture d’une Pull Request** sur GitHub pour fusionner la fonctionnalité dans `develop`.

### **Fix d’un Bug**

1. **Création de la branche de bugfix** à partir de `develop` :

```shell
git checkout -b bugfix/fix-login-error develop
```

1. **Correction du bug**, puis **commit et push**.

2. **Ouverture d’une Pull Request** pour fusionner la branche de bugfix dans `develop`.

3. Si le bug est critique, fusionner également dans `main` et taguer la version :

4. 2. Si le bug est critique, fusionner également dans `main` et taguer la version :

```shell
git checkout main
git merge bugfix/fix-login-error
git tag -a v1.0.1 -m "Hotfix: Fixed login issue"
git push origin main --tags
```

---

## 🧰 **Suppression des Branches**

Après fusion, il est recommandé de supprimer les branches pour garder le dépôt propre :

```shell
git branch -d feature/authentication
git branch -d bugfix/fix-login-error
git push origin --delete feature/authentication
git push origin --delete bugfix/fix-login-error
```

## 🎯 **Meilleures Pratiques**

- **Ne fusionnez pas de code sans passer par les PR**.
- **Faites des commits fréquents** et ajoutez des messages clairs pour chaque modification.
- **Mettez à jour `develop` régulièrement** avec les dernières modifications de `main`.

## 🌟 **Conclusion**

La gestion rigoureuse des branches est essentielle pour maintenir un développement fluide, une intégration continue stable, et un déploiement rapide et sûr. Suivez cette stratégie pour garantir la qualité et la cohérence du code tout au long du cycle de vie du projet.
