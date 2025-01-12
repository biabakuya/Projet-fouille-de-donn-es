# **Analyse des Étudiants Internationaux - Projet de Fouille de Données**

Ce projet explore les données relatives à la mobilité des étudiants internationaux dans différents pays. L'objectif est de comprendre les tendances, d'identifier les principaux facteurs influençant cette mobilité, et de modéliser des groupes ou clusters pour des analyses approfondies.

---

## **1. Contexte**

La mobilité internationale des étudiants est un sujet clé pour comprendre les dynamiques globales de l'éducation. Ce projet se concentre sur :
- L'identification des pays attirant le plus d'étudiants internationaux.
- L'étude des caractéristiques associées à cette mobilité, comme les indicateurs de performance des étudiants (notes moyennes) et les caractéristiques des pays.
- L'application de techniques de fouille de données pour dégager des insights exploitables.

Le jeu de données contient **5557 lignes** représentant les étudiants internationaux répartis entre plusieurs pays, avec **10 variables** décrivant leurs caractéristiques, comme :
- **Pays** : Le pays d'accueil.
- **Value** : Le nombre d'étudiants internationaux.
- **Notes moyennes** : Moyennes des résultats scolaires des étudiants.
- **Indicateurs** : Variables qualitatives décrivant les caractéristiques académiques.

---

## **2. Objectifs**

Les principaux objectifs du projet sont :
1. **Comprendre les données** :
   - Explorer les distributions des variables.
   - Analyser les relations entre variables.
2. **Créer des clusters** :
   - Grouper les pays ou les étudiants ayant des caractéristiques similaires.
3. **Modéliser des groupes prédictifs** :
   - Utiliser des modèles supervisés pour prédire la classification des données.
4. **Interpréter les résultats** :
   - Fournir des insights exploitables pour les décideurs (universités, gouvernements).

---

## **3. Étapes du Projet**

### **Étape 1 : Préparation des Données**
- **Chargement et nettoyage :**
  - Gestion des valeurs manquantes par imputation ou suppression.
  - Encodage des variables catégorielles (e.g., `Indicateur`, `Pays`).
- **Transformation des données :**
  - Normalisation des variables numériques avec `StandardScaler`.

---

### **Étape 2 : Analyse Exploratoire**
- **Distribution des étudiants par pays :**
  - Identifier les pays recevant le plus d'étudiants internationaux.
  - Visualisation avec des graphiques en barres et des diagrammes circulaires.
- **Analyse des notes moyennes :**
  - Étude des statistiques descriptives des résultats scolaires.
  - Vérification de la normalité des variables avec des tests statistiques et des histogrammes.
- **Relations entre variables :**
  - Matrice de corrélation.
  - Nuages de points pour les relations clés (e.g., entre `Value` et `Notes moyennes`).

---

### **Étape 3 : Clustering**
- **K-Means :**
  - Détection des groupes dans les données en fonction des caractéristiques des pays.
  - Détermination du nombre optimal de clusters grâce au score de silhouette.
- **Classification Hiérarchique Ascendante (CAH) :**
  - Construction d'un dendrogramme pour une visualisation hiérarchique des relations entre les pays.
  - Découpage des clusters à différentes hauteurs pour une analyse fine.

---

### **Étape 4 : Modélisation Supervisée**
- **Modèles testés :**
  - Régression Logistique.
  - Naive Bayes.
  - Random Forest.
- **Processus :**
  - Entraînement des modèles sur des groupes identifiés par K-Means.
  - Évaluation des performances à l'aide de métriques comme la précision, le rappel et le F1-score.
- **Comparaison des modèles :**
  - Identification du meilleur modèle pour prédire la répartition des étudiants par cluster.

---

### **Étape 5 : Résultats et Insights**
- **Résultats Clés :**
  - Les clusters identifiés montrent des groupes distincts de pays attirant des étudiants avec des caractéristiques similaires.
  - Le modèle **Random Forest** s'est avéré le plus performant avec une précision globale élevée.
- **Insights :**
  - Certains pays attirent une majorité d'étudiants en raison de leur excellence académique ou de leur attractivité économique.
  - Les erreurs communes entre modèles indiquent des groupes d'étudiants ou de pays plus difficiles à classifier, nécessitant une analyse plus fine.


Auteur: BIABA KUYA Jirince
