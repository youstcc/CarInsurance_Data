# Car Insurance Prediction

Ce projet a pour objectif de développer un modèle de prédiction des coûts d'assurance automobile (variable continue outcome), puis d’explorer une version classification binaire (sinistre / pas de sinistre). Il utilise scikit-learn pour le prétraitement, l’entraînement et l’évaluation des modèles.

##📂 Structure du projet

````
PythonProject [CarInsurance_Data]/
├── .venv/                 # Environnement virtuel Python
├── data/                  # Données brutes et décrites
│   ├── car_insurance.csv  # Jeu de données principal
│   └── car_insurance_desc.pdf
├── models/                # Modèles sauvegardés (.pkl)
├── notebooks/
│   └── 01_exploration.ipynb   # Notebook d’exploration et modélisation
├── README.md              # Documentation du projet (ce fichier)
└── requirements.txt       # Dépendances Python
````

## 🚀 Installation

- Cloner le dépôt :

````
git clone https://github.com/youstcc/CarInsurance_Data.git
cd PythonProject
````

- Créer et activer l’environnement :

````
python3 -m venv .venv
# Linux / macOS
source .venv/bin/activate
# Windows PowerShell
.\.venv\Scripts\activate
````

- Installer les dépendances :

````
pip install --upgrade pip
pip install -r requirements.txt
````
Prérequis : Python >= 3.8, pip, git.

## 🗂️ Contenu des dossiers

**data/ :**

````
car_insurance.csv : données brutes (âges, crédit, infractions, etc.).
car_insurance_desc.pdf : description des variables.
````
**notebooks/ :**

````
01_exploration.ipynb :

Chargement et exploration initiale (statistiques, distributions, valeurs manquantes).
Prétraitement : imputation, encodage, détection d’outliers, normalisation.
Modélisation : régression linéaire, validation croisée, comparaison de modèles.
Classification binaire : régression logistique, perceptron, KNN.
````

**Autres pickles si nécessaires.**

````
requirements.txt : lister les packages Python (pandas, scikit-learn, matplotlib, etc.).
````

## 📖 Utilisation

**1. Exploration & prétraitement via notebook**

- jupyter lab notebooks/01_exploration.ipynb

- Suivez les cellules pour explorer, nettoyer et modéliser.

**2. Pipeline complet en ligne de commande**

- python main.py --data data/car_insurance.csv --output models/best_model_rf.pkl

Options:

--data : chemin vers le CSV.

## 📊 Résultats clés

LogisticRegression (meilleur compromis) :

* Accuracy ≃ 0.80

* Précision ≃ 0.74, Rappel ≃ 0.59, F1 ≃ 0.66

* Validation croisée (5 plis) : 0.80 ± 0.01

* Perceptron : moins performant (accuracy ≃ 0.75, std CV ≃ 0.05)

* K‑Nearest Neighbors (k=5) : overfitting léger (train 0.84 vs test 0.78), CV 0.78 ± 0.007

## 🎯 Pistes d’amélioration

* Optimiser les hyperparamètres via GridSearchCV / RandomizedSearchCV.

* Tester d’autres algorithmes : Random Forest, XGBoost, LightGBM.

* Enrichir les features : interactions, encodage target, PCA.

* Ajuster le seuil de décision pour maximiser le rappel ou la précision selon le coût métier.

## 🤝 Contribuer

Les contributions sont les bienvenues :

**Forkez ce dépôt.**

- Créez une branche (git checkout -b feature/ma-feature).

- Commit (git commit -am 'Ajout de ma feature').

- Push (git push origin feature/ma-feature).

- Ouvrez une Pull Request.

## 📄 Licence

IMT Nord Europe

- Youri STECKO
- steckoyouri@gmail.com

- Bahir BOUDOUMA
- boudoumabahir@gmail.com

