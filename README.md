﻿# 🚀 runtrack_java_spring-jour1-
## 📅 Job 01

### ❓ Question : Qu'est-ce que Spring Initializr et comment peut-il faciliter la création d'un nouveau projet Spring ?

Spring Initializr est un générateur de projet pour configurer rapidement une application Spring Boot avec les dépendances nécessaires.

---

## 📅 Job 02

### ❓ Question : Pourquoi le fichier `pom.xml` est-il crucial dans un projet Maven ?

Il gère les dépendances, la configuration du build et les plugins Maven nécessaires au projet.

---

## 📅 Job 03

### ❓ Question : Qu'est-ce qu'un contrôleur dans le contexte de Spring MVC ?

C’est une classe qui gère les requêtes HTTP et retourne des réponses (HTML, JSON, texte…) en exposant un service.

---

## 📅 Job 04

### ❓ Question : Comment Spring permet-il l'injection de propriétés depuis des fichiers de configuration ?

Spring utilise l'injection de dépendances pour injecter les valeurs des propriétés définies dans les fichiers de configuration (`application.properties` ou `application.yml`) grâce à l’annotation `@Value` ou via des classes de configuration annotées avec `@ConfigurationProperties`.

📦 **Détail technique** :
- Spring Boot charge automatiquement les fichiers `application.properties` ou `application.yml` lors du démarrage.
- Ces fichiers sont placés dans `src/main/resources`.

🔧 **Exemple avec `@Value`** :
```java
@Value("${greeting.message}")
private String greetingMessage;
```
---
## 📅 Job 05

### ❓ Question : Pourquoi serait-il utile d'avoir différents profils dans une application Spring ?

Les profils Spring permettent de gérer plusieurs environnements (développement, test, production, etc.) avec des configurations adaptées à chacun.

🔍 **Détails et avantages** :

| Environnement | Utilité du profil Spring |
|---------------|---------------------------|
| `dev`         | Activer les logs détaillés, utiliser une base en mémoire, charger des mocks |
| `test`        | Simuler des services externes, isoler la base de test |
| `prod`        | Charger les vraies bases de données, config sécurisée |
| `staging`     | Tester une version avant la mise en production |

📅 **Concrètement, un profil permet de** :
- Changer les URLs (ex: base de données, API externe)
- Modifier les paramètres de sécurité ou de cache
- Activer ou désactiver certains beans/services avec `@Profile`
- Afficher des messages différents dans l’application

---

## 📅 Job 06

### ❓ Question : En quoi la dépendance DevTools est-elle bénéfique pour le développement ?

La dépendance **Spring Boot DevTools** améliore l’expérience de développement en offrant des fonctionnalités automatiques comme :
- Le **rechargement à chaud (hot restart)**
- La **désactivation du cache** (Thymeleaf, etc.)
- Le **LiveReload** pour actualiser automatiquement le navigateur

🚀 **Avantages principaux de `spring-boot-devtools` :**

| 🔧 Fonctionnalité                     | ⚡ Explication |
|--------------------------------------|----------------|
| ✅ Reload automatique (Hot restart)  | Redémarre l’application à chaque changement de fichier `.class`, sans redémarrage manuel |
| ✅ LiveReload                        | Rafraîchit automatiquement le navigateur (si plugin actif) |
| ✅ Désactivation du cache            | Recharge les vues HTML à chaque modification |
| ✅ Log amélioré au redémarrage       | Affiche clairement les modifications |
| ✅ Séparation des configs dev/prod   | Désactive certains comportements en production |

---
