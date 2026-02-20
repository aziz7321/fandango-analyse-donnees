# 🎬 Analyse des Biais de Notation sur Fandango

![Python](https://img.shields.io/badge/Python-3.8+-blue?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)
![Pandas](https://img.shields.io/badge/Pandas-2.0+-150458?logo=pandas)
![Seaborn](https://img.shields.io/badge/Seaborn-0.12+-3776AB?logo=python)

## 📝 Contexte

Ce projet est une réplication et une analyse approfondie de l'enquête du site **FiveThirtyEight** concernant les pratiques de notation de la plateforme de vente de billets de cinéma **Fandango**.

**Problématique :** Peut-on faire confiance aux notes d'une plateforme qui a un intérêt financier à ce que les films soient bien notés ?

## 🎯 Questions Clés

1. **Biais interne** : Y a-t-il une différence entre la note calculée (`RATING`) et la note affichée (`STARS`) sur Fandango ?
2. **Biais externe** : Les notes de Fandango sont-elles systématiquement plus hautes que celles des autres plateformes ?
3. **Cas extrêmes** : Comment Fandango note-t-il les films que les critiques mondiales considèrent comme "mauvais" ?

## 🛠️ Méthodologie et Outils

- **Langage** : Python
- **Librairies** :
  - `pandas` & `numpy` : Manipulation et nettoyage des données
  - `matplotlib` & `seaborn` : Visualisation des données
- **Données** : Datasets de FiveThirtyEight comparant Fandango à Rotten Tomatoes, Metacritic et IMDB

## 📊 Résultats Clés

### 1. Le Biais d'Arrondi de Fandango

L'analyse révèle un décalage systématique entre les notes réelles (`RATING`) et les étoiles affichées (`STARS`). Fandango arrondit presque toujours à l'unité supérieure.

### 2. Comparaison Multi-Plateformes

Après normalisation sur une échelle de 0 à 5, on observe que Fandango ne descend quasiment jamais en dessous de 3 étoiles, contrairement aux autres sites qui présentent une distribution en cloche classique.

### 3. Analyse des "Pires Films"

Les films les plus mal notés par les critiques conservent des notes étonnamment élevées sur Fandango (3/5 ou plus), confirmant le biais de la plateforme.

## ✅ Conclusion

Ce projet démontre une corrélation entre l'intérêt commercial et la présentation des données. Les notes de Fandango sont biaisées à la hausse, rendant la plateforme peu fiable pour un jugement critique objectif.

## 🚀 Comment exécuter ce projet

1. **Cloner le dépôt**
   ```bash
   git clone https://github.com/aziz7321/fandango-analyse-donnees.git
   cd fandango-analyse-donnees

2. **Installer les dépendances**
   ``` bash
   pip install -r requirements.txt

3. **Lancer le notebook**

   ``` bash
   jupyter notebook notebooks/Projet_Python.ipynb

## 📁 Structure du Projet 
  ### text
  ### ├── data/               # Données brutes CSV
  ### ├── notebooks/          # Notebook Jupyter d'analyse
  ### ├── docs/               # Rapport PDF
  ### ├── images/             # Graphiques générés
  ### ├── requirements.txt    # Dépendances Python
  ### └── README.md           # Documentation du projet

## 👤 Auteur
 ### Abdoulaziz Keita - GitHub

## 📚 Sources
 ### https://fivethirtyeight.com/features/fandango-movies-ratings/ #Enquête originale de FiveThirtyEight
 ### https://github.com/fivethirtyeight/data/tree/master/fandango  #Données utilisées