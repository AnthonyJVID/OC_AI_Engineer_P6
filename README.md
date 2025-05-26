# 🛒 OC - Projet 6 : Classifiez automatiquement des biens de consommation

Ce projet est réalisé dans le cadre du parcours *AI Engineer* d’OpenClassrooms.  
Il s’inscrit dans une mission au sein de l’entreprise fictive **Place de Marché**, qui souhaite développer un **moteur de classification automatique** de produits d’après leurs images et descriptions textuelles.

---

## 🎯 Objectifs

1. **Étudier la faisabilité** d’un moteur de classification automatique (image + texte)
2. **Développer une solution de classification supervisée** à partir des images
3. **Expérimenter une API externe** pour enrichir la base de produits

---

## 📂 Contenu du projet

### 1. Faisabilité & Extraction de features (`1_notebook_pretraitement_feature_extraction_faisaibilite_122024.ipynb`)

- Prétraitement des données texte et image
- Extraction des features :
  - Texte : Bag-of-Words, TF-IDF, Word2Vec, USE, BERT
  - Image : SIFT, ORB, CNN (Transfer Learning)
- Réduction de dimension (TSNE, PCA) et visualisation 2D
- Évaluation par clustering non supervisé et similarité des regroupements
- Conclusion sur la **faisabilité du regroupement automatique**

---

### 2. Classification supervisée d’images (`2_notebook_classification_122024.ipynb`)

- Réutilisation de CNN (transfer learning avec fine-tuning)
- Application de **data augmentation** pour améliorer les performances
- Entraînement et évaluation du modèle sur les classes disponibles
- Visualisations des performances et erreurs de classification

---

### 3. Enrichissement via API externe (`3_script_Python_122024.ipynb`)

- Utilisation de l’**API Open Food Facts** (produits contenant le mot-clé *champagne*)
- Extraction des champs : `foodId`, `label`, `category`, `foodContentsLabel`, `image`
- Sauvegarde des résultats dans un fichier `.csv` compatible avec les futurs modèles

---

## 🗂️ Structure du dépôt

```
├── 1_notebook_pretraitement_feature_extraction_faisaibilite_122024.ipynb  → Extraction de features et clustering
├── 2_notebook_classification_122024.ipynb                                 → Classification supervisée avec data augmentation
├── 3_script_Python_122024.ipynb                                           → Appel API Open Food Facts et export CSV
├── data/                                                                  → Dataset d’images et descriptions
├── presentation.pdf                                                       → Synthèse des résultats (30 slides max)
└── README.md                                                              → Présentation du projet
```

---

## 🛠️ Technologies utilisées

- Python
- Jupyter Notebook
- `scikit-learn`, `tensorflow.keras`, `OpenCV`, `transformers`, `gensim`, `matplotlib`, `seaborn`
- API : Open Food Facts

---

## 🧠 Auteur

Projet réalisé par **AnthonyJVID** dans le cadre du parcours *AI Engineer* chez OpenClassrooms.

---

## 📄 Licence

Projet pédagogique basé sur des données et API publiques sans contrainte de propriété intellectuelle.
