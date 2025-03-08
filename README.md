# 📊 Projet d'Évaluation - Traitement et Visualisation des Données

Bienvenue dans ce projet de **traitement, anonymisation, transformation et visualisation** de données e-commerce.

## 🎯 Objectif du Projet
L’objectif de ce projet est d’aider une entreprise e-commerce fictive à mieux **exploiter ses données clients et transactions** tout en respectant le RGPD.

## 🚀 Ce que nous avons mis en place :
✅ Un **pipeline automatisé** sous **Apache NiFi** pour anonymiser et nettoyer les données.
✅ Une **sortie de données optimisée** pour Power BI.
✅ Un **tableau de bord interactif** pour visualiser les tendances de vente et comportements clients.

En combinant **Python, Apache NiFi et Power BI**, nous avons conçu une solution robuste pour analyser les données transactionnelles et les comportements des clients.

---

## 🏗 **Architecture du Pipeline**

### 🔹 **1. Extraction des données**
- **Source des données** : Fichier CSV contenant des informations client et transactionnelles.
- 📍 **Lecture automatisée** via **GetFile** dans NiFi.

### 🔹 **2. Transformation et nettoyage**
- 🛠 **Technologies** : Python (pandas, numpy, faker)
- ✅ **Actions réalisées** :
  - Anonymisation des données sensibles (noms, emails, cartes bancaires).
  - Correction des valeurs manquantes et aberrantes.
  - Agrégation et création de nouvelles variables utiles pour l’analyse.

### 🔹 **3. Intégration dans Apache NiFi**
- 🔄 **Processus de traitement** :
  - `GetFile` : Lecture du fichier brut.
  - `ExecuteStreamCommand` : Exécution du script Python pour l’anonymisation et le nettoyage.
  - `PutFile` : Export des données nettoyées.
- 📌 **Configurations mises en place** :
  - Définition des paramètres des processors NiFi avec gestion des chemins et arguments.

### 🔹 **4. Visualisation et Reporting avec Power BI**
- 📊 **Tableau de bord interactif** comprenant :
  - Analyse des comportements clients (fréquence d'achat, panier moyen).
  - Tendances des achats en fonction du temps.
  - Répartition des ventes par produit et catégorie.
- 🔍 **Ajout de filtres interactifs pour une analyse dynamique.**

---

## 📂 Structure du Projet
```
projet_nifi/
│── script_nifi.py           # Script Python pour l’anonymisation et transformation des données
│── dataset_projet_evaluation.csv  # Fichier brut en entrée
│── cleaned_transactions.csv  # Fichier nettoyé en sortie du pipeline
│── PowerBI_Dashboard/       # Contient le fichier .pbix du tableau de bord Power BI
│── NiFi_Flow/               # Contient le flow NiFi exporté
│── README.md                # Documentation du projet
```

---

## 🚀 Installation et Exécution

### 📌 Prérequis
- **Apache NiFi** installé et configuré.
- **Python 3.12** avec les bibliothèques suivantes :
  ```bash
  pip install pandas numpy faker
  ```
- **Power BI Desktop** pour la visualisation des données.

### 🔹 Lancer le pipeline NiFi
1. **Démarrer Apache NiFi** :
   - Accédez à `http://localhost:8080/nifi`
   - Importer le flow **NiFi_Flow**.
2. Vérifiez que tous les processors (`GetFile`, `ExecuteStreamCommand`, `PutFile`) sont bien configurés.
3. Démarrer le pipeline et surveiller les logs.

### 🔹 Exécuter le script Python indépendamment
```bash
python script_nifi.py
```

### 🔹 Charger les données dans Power BI
1. Ouvrir **Power BI Desktop**.
2. Importer le fichier **cleaned_transactions.csv**.
3. Mettre à jour les visualisations et interagir avec les filtres.

---

## 📝 Contributions
Les contributions sont les bienvenues ! Merci de soumettre une **Pull Request** ou d’ouvrir une **Issue** pour toute suggestion ou amélioration.

---

## 📜 Licence
Ce projet est sous licence MIT - voir le fichier [LICENSE](LICENSE) pour plus de détails.

---

## 🙌 Remerciements
Merci à notre équipe de développement et à nos professeurs pour leur accompagnement sur ce projet ! 🎉
