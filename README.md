# 🏦 Projet : Prédiction du Risque de Défaut de Paiement Client (Crédit Bancaire)

Ce dépôt présente un projet de Machine Learning axé sur la **prédiction du risque de défaut de paiement** chez les clients bancaires. L'objectif est de doter les institutions financières d'un outil prédictif robuste pour affiner leurs décisions d'octroi de crédit, optimiser la gestion des risques et réduire les pertes potentielles.

---

### 🎯 Objectif du Projet

L'enjeu principal de ce projet est de développer un modèle capable d'identifier avec précision les clients susceptibles de faire défaut sur leurs remboursements de prêt. Une prédiction fiable permet :
* **D'améliorer la prise de décision :** Accorder des crédits de manière plus éclairée.
* **De minimiser les risques :** Réduire l'exposition aux prêts non performants.
* **D'optimiser les stratégies :** Allouer les ressources de manière plus efficace pour le recouvrement ou la prévention.

---

### 📊 Données Utilisées

Le modèle a été construit sur un jeu de données synthétique (mais représentatif) de clients bancaires. Il inclut des caractéristiques essentielles comme :

* **Informations Démographiques :** `Age`, `Ville`
* **Informations Financières :** `Revenu_Mensuel`, `Dette_Actuelle`, `Nb_Credits_Actifs`, `Taux_Interet_Moyen_Credits`
* **Historique Client :** `Anciennete_Client_Mois`, `Historique_Paiement` (`Excellent`, `Bon`, `Mauvais`)
* **Détails du Prêt :** `Type_Contrat_Pret` (`Consommation`, `Immobilier`, `Automobile`, etc.)
* **Statut Actuel :** `Statut_Emploi` (`Salarié`, `Sans Emploi`, `Freelance`, etc.)
* **Variable Cible :** `Defaut_Paiement` (0 = Non-défaut, 1 = Défaut)

---

### 🚀 Méthodologie et Compétences Appliquées

Ce projet met en œuvre un pipeline complet d'analyse de données et de Machine Learning :

1.  **Exploration de Données (EDA) :**
    * Analyse des distributions des variables (numériques et catégorielles).
    * Identification des corrélations et des relations potentielles entre les caractéristiques et le défaut de paiement.

2.  **Prétraitement et Ingénierie des Caractéristiques :**
    * **Gestion des valeurs manquantes :** Traitement des éventuelles données manquantes.
    * **Encodage des variables catégorielles :** Conversion des variables comme `Type_Contrat_Pret`, `Statut_Emploi`, `Historique_Paiement`, et `Ville` en formats numériques exploitables par le modèle.
    * **Standardisation/Normalisation :** Mise à l'échelle des variables numériques (`Age`, `Revenu_Mensuel`, `Dette_Actuelle`, etc.) pour assurer une performance optimale du modèle.

3.  **Modélisation Prédictive :**
    * **Sélection du modèle :** Utilisation d'un algorithme de classification adapté: Régression Logistique.
    * **Entraînement et Validation :** Division du jeu de données en ensembles d'entraînement et de test pour évaluer la capacité de généralisation du modèle.

4.  **Évaluation Détaillée du Modèle :**
    * **Métriques Clés :** Analyse approfondie de l'Accuracy, de la Précision, du Rappel et du F1-score.
    * **Matrice de Confusion :** Interprétation des Vrais Positifs, Vrais Négatifs, Faux Positifs et Faux Négatifs pour comprendre les types d'erreurs et leur impact métier.
    * **Robustesse :** Analyse de la performance sur la classe minoritaire (les cas de défaut de paiement) pour s'assurer que le modèle ne sous-estime pas ce risque crucial.

---

### ✨ Résultats Clés

Le modèle développé démontre une **performance prédictive exceptionnelle** :

* **Accuracy sur l'ensemble de test : 98%**, indiquant une très grande fiabilité des prédictions.
* **Excellente généralisation :** Le score sur l'ensemble de test (0.98) est cohérent avec celui de l'entraînement (0.97), prouvant un **ajustement optimal** et l'absence de sur-apprentissage.
* **Identification précise des risques :** La matrice de confusion révèle une capacité remarquable à distinguer les cas de défaut de paiement des non-défauts, avec des scores de Précision et de Rappel très élevés (autour de 97-98%) pour les deux classes. Les erreurs de classification sont minimes (seulement 2 erreurs sur 100 observations testées).

Ces résultats confirment la capacité du modèle à être un atout stratégique pour l'évaluation et la gestion du risque client.

---

### 🛠️ Technologies Utilisées

* **Langage :** Python
* **Bibliothèques :** `Pandas`, `NumPy`, `Scikit-learn`, `Matplotlib`, `Seaborn`
* **Environnement :** Jupyter Notebook (ou Google Colab)

---

