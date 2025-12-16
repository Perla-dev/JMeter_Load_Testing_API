# 📈 Performance Testing and Load Simulation for REST API (JMeter)

## 🎯 Aperçu du Projet

Ce projet contient les artefacts nécessaires pour simuler une **montée en charge** sur une API REST. Le but est d'évaluer la **capacité de l'API à supporter un trafic important** et d'identifier les goulots d'étranglement ou les problèmes de performance avant le déploiement en production.

## 🔑 Compétences et Outils Démontrés

| Domaine | Outils et Technologies |
| :--- | :--- |
| **Outil de Performance** | [cite_start]**Apache JMeter** (Création et exécution de plans de test de charge)[cite: 33]. |
| **Tests Ciblés** | [cite_start]Tests de Performance (Montée en charge), Tests de Stress, Tests d'API[cite: 11, 38]. |
| **Protocoles** | [cite_start]HTTP Request Samplers (simulation des requêtes d'API REST). |
| **Analyse** | [cite_start]Utilisation des Listeners (Aggregate Report, Summary Report) pour l'analyse des temps de réponse et du débit (Throughput)[cite: 12]. |
| **Processus** | [cite_start]Définition des objectifs de performance et contribution à la décision **Go / No Go** en fonction des résultats[cite: 15]. |

## ⚙️ Structure du Plan de Test (`.jmx`)

Le plan de test (`load_test_scenario.jmx`) est structuré pour simuler une utilisation réaliste :

1.  **Thread Group (Simulation de charge) :** Configuration du nombre d'utilisateurs concurrents (Threads), de la période de montée en charge (Ramp-Up), et de la durée du test.
2.  **HTTP Request Samplers :** Envoi de requêtes spécifiques (GET, POST, etc.) aux différents endpoints de l'API. Les requêtes simulent des scénarios utilisateur clés (ex. : lecture de données, soumission de formulaire).
3.  **Assertions :** Vérification du code de réponse HTTP (ex. : 200 OK) pour s'assurer du fonctionnement correct de l'API sous contrainte.
4.  **Listeners :** Collecte et affichage des données de performance (latence, erreurs, débit).

## 📊 Principaux Indicateurs (Métriques) Analysés

* **Temps de Réponse Moyen (Average Response Time) :** Durée moyenne nécessaire pour recevoir une réponse de l'API.
* **Débit (Throughput) :** Nombre de requêtes traitées par seconde (indicateur de capacité).
* **Taux d'Erreur :** Pourcentage des requêtes ayant échoué sous la charge (indicateur de stabilité).

## ▶️ Comment Exécuter les Tests

### Prérequis

* Java Runtime Environment (JRE) installé.
* Apache JMeter installé.
* L'URL d'une API de démonstration ou d'un environnement de test.

### Étapes d'exécution

1.  Cloner le dépôt : `git clone https://github.com/Perla-dev/JMeter_Load_Testing_API.git`
2.  Ouvrir JMeter.
3.  Ouvrir le fichier `.jmx` dans JMeter (File -> Open -> `load_test_scenario.jmx`).
4.  Modifier l'adresse IP/URL de l'API cible si nécessaire.
5.  Démarrer le test (Run -> Start).
