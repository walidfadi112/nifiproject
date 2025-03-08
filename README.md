# nifiproject
Bien sûr ! Voici ton **README.md** formaté en Markdown, prêt à être posé directement sur **GitHub** :

---

```md
# 📊 Projet d'Évaluation - Traitement et Visualisation des Données  

Bienvenue dans ce projet de **traitement, anonymisation, transformation et visualisation** de données e-commerce, où nous avons construit un **pipeline automatisé de bout en bout**.

## 🎯 Objectif du Projet  
L’objectif de ce projet est d’aider une entreprise e-commerce fictive à mieux **exploiter ses données clients et transactions** tout en respectant le **RGPD**.  

### 🚀 Ce que nous avons mis en place :
✅ Un **pipeline automatisé** sous **Apache NiFi** pour anonymiser et nettoyer les données.  
✅ Une **sortie de données optimisée** pour Power BI.  
✅ Un **tableau de bord interactif** pour visualiser les tendances de vente et comportements clients.  

En combinant **Python, Apache NiFi et Power BI**, nous avons conçu une solution robuste pour analyser les données commerciales.  

---

## 🏗️ **Architecture du Pipeline**  
### 🔹 **1. Extraction des données**
📍 **Source des données** : Fichier CSV contenant des informations client et transactionnelles.  
📍 **Lecture automatisée** via **GetFile** dans NiFi.  

### 🔹 **2. Transformation et nettoyage**
📍 **Python (pandas, numpy, faker)** pour l’anonymisation et le nettoyage.  
📍 **Actions réalisées** :  
   - Anonymisation des données sensibles (noms, emails, cartes bancaires).  
   - Correction des valeurs manquantes et aberrantes.  
   - Agrégation et création de nouvelles colonnes utiles pour l’analyse.  

### 🔹 **3. Chargement et stockage**
📍 **Export des données nettoyées** dans un fichier CSV prêt pour Power BI via **PutFile** dans NiFi.  

### 🔹 **4. Visualisation et analyse**
📍 **Power BI** est utilisé pour analyser et présenter les insights à travers un **tableau de bord interactif**.  

---

## ⚙️ **Technologies et outils utilisés**  

| Technologie | Rôle |
|------------|------|
| **Python** | Chargement, nettoyage et anonymisation des données |
| **Apache NiFi** | Automatisation du pipeline de traitement des données |
| **Power BI** | Analyse et visualisation des données |
| **CSV** | Format d’entrée et de sortie des données |

---

## 📂 **Structure du Projet**  

```
📁 projet_nifi
│── 📄 script_nifi.py          # Script Python pour l’anonymisation et transformation des données
│── 📄 cleaned_transactions.csv # Fichier nettoyé en sortie du pipeline
│── 📄 dataset_projet_evaluation.csv # Fichier brut en entrée
│── 📁 PowerBI_Dashboard       # Contient le fichier .pbix du tableau de bord Power BI
│── 📁 NiFi_Flow               # Contient le flow NiFi exporté
│── 📄 README.md               # Documentation du projet
```

---

## 🚀 **Guide d’Installation et d’Utilisation**

### 1️⃣ **Installation des Prérequis**
Avant de commencer, assurez-vous d’avoir installé :
- **Python 3.12** ([Télécharger ici](https://www.python.org/downloads/))
- **Apache NiFi** ([Télécharger ici](https://nifi.apache.org/download.html))
- **Power BI Desktop** ([Télécharger ici](https://powerbi.microsoft.com/fr-fr/downloads/))

### 2️⃣ **Installation des bibliothèques Python**
Ouvrez un terminal et exécutez :
```sh
pip install pandas numpy faker
```

---

## 🏗️ **Mise en place du pipeline Apache NiFi**

### 🔹 **Configuration des Processors NiFi**
| Processor | Configuration |
|-----------|--------------|
| **GetFile** | Charge le fichier brut `dataset_projet_evaluation.csv` |
| **ExecuteStreamCommand** | Exécute le script Python pour transformation des données |
| **PutFile** | Sauvegarde le fichier nettoyé `cleaned_transactions.csv` |

### 🔹 **Comment exécuter le pipeline ?**
1. **Lancer Apache NiFi** en exécutant `run-nifi.bat` sous Windows ou `bin/nifi.sh start` sous Linux.  
2. **Importer le flow NiFi** depuis `conf/flow.json.gz` ou reconstruire les processors manuellement.  
3. **Démarrer les processors** en cliquant sur **Start** pour lancer le pipeline.  

---

## 🖥️ **Exécution du Script Python**
Si vous souhaitez exécuter **script_nifi.py** indépendamment :
```sh
python script_nifi.py
```
Le fichier **cleaned_transactions.csv** sera généré avec les données anonymisées et nettoyées.

---

## 📊 **Analyse et Visualisation avec Power BI**  

### 🔹 **Comment importer les données dans Power BI ?**
1. **Ouvrir Power BI Desktop**  
2. **Importer `cleaned_transactions.csv`** en tant que source de données.  
3. **Créer des relations** entre les tables si nécessaire.  
4. **Construire des visualisations interactives**.  

### 🔹 **Visualisations incluses**
✅ **Répartition des ventes** par produit  
✅ **Tendances des achats** au fil du temps  
✅ **Carte géographique interactive**  

---

## 🛠️ **Dépannage et Problèmes Connus**

❌ **Erreur : `dataset_projet_evaluation.csv` introuvable**  
➡️ Vérifiez que le fichier existe et que **GetFile** pointe vers le bon répertoire.  

❌ **Erreur : Power BI ne charge pas le fichier**  
➡️ Vérifiez que **cleaned_transactions.csv** a bien été généré et contient des données valides.  

❌ **Erreur d’exécution du script Python dans NiFi**  
➡️ Assurez-vous que `ExecuteStreamCommand` est bien configuré avec `python.exe` et `script_nifi.py`.  

---

## 🏆 **Résultats et Insights**

Grâce à cette approche, nous avons :
✅ Un **pipeline automatisé** et efficace.  
✅ Des **données nettoyées et anonymisées** conformes au RGPD.  
✅ Un **tableau de bord interactif** offrant une vision claire des tendances.  

---

## 🤝 **Auteurs et Collaboration**
Projet réalisé par :
- **Nom 1**
- **Nom 2**
- **Nom 3**

📌 Ce projet a été développé dans le cadre d'une évaluation académique.  

🔥 **Merci d’avoir suivi ce projet ! N’hésitez pas à proposer des améliorations 🚀**
```

---

### 📌 **Pourquoi ce README est-il prêt pour GitHub ?**
- Il est **clair, structuré et bien formaté** en **Markdown**.
- Il contient des **titres (h1, h2, h3)** pour une meilleure lisibilité.
- Il inclut des **tableaux, des listes à puces et des liens cliquables**.
- Il est **facile à copier-coller** et à publier directement sur **GitHub**.

Tu peux le copier tel quel et l’intégrer dans ton projet sur **GitHub** ! 🚀  
Si tu veux des modifications ou ajouts, dis-moi ! 😊
