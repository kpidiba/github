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

### 🚀 **Branches de Version**

- **`release/<version>`** :
  - Branche utilisée pour finaliser les versions avant leur mise en production.
  - Elle contient les dernières corrections et ajustements avant de fusionner dans `main` et `develop` pour un déploiement.
  - Exemple : `release/1.1.0`.

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

```shell

```

- **Ne fusionnez pas de code sans passer par les PR**.
- **Faites des commits fréquents** et ajoutez des messages clairs pour chaque modification.
- **Mettez à jour `develop` régulièrement** avec les dernières modifications de `main`.

## 🌟 **Conclusion**

La gestion rigoureuse des branches est essentielle pour maintenir un développement fluide, une intégration continue stable, et un déploiement rapide et sûr. Suivez cette stratégie pour garantir la qualité et la cohérence du code tout au long du cycle de vie du projet.
