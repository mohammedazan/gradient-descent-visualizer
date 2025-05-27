# Application Graphique de Descente de Gradient pour la Régression et la Classification

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=white" alt="Django">
  <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white" alt="Scikit-learn">
  <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas">
  <img src="https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge&logo=matplotlib&logoColor=white" alt="Matplotlib">
  <img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white" alt="GitHub">
</p>

---
---

## 📖 Table des matières

1. [🎯 Contexte & Objectifs](#-contexte--objectifs)
2. [🔥 Fonctionnalités](#-fonctionnalités)
3. [⚙️ Stack Technique](#️-stack-technique)
4. [🏗️ Architecture & Conception](#️-architecture--conception)
5. [🔧 Installation & Lancement](#-installation--lancement)
6. [🎮 Guide d’Utilisation](#-guide-dutilisation)
7. [🔍 Paramétrage & Optimisation](#-paramétrage--optimisation)
8. [📂 Organisation du Code](#-organisation-du-code)
9. [🤝 Contribution & Workflow Git](#-contribution--workflow-git)
10. [🖼️ Présentation & Poster](#️-présentation--poster)
11. [📜 Licence](#-licence)

---

## 🎯 Contexte & Objectifs

Ce projet, réalisé dans le cadre du module **Machine Learning**, a pour vocation de **rendre la descente de gradient** accessible et **intuitive**. Grâce à une interface graphique soignée, tout utilisateur (débutant ou expert) peut :

* Importer et explorer un dataset
* Prétraiter les données (imputation, normalisation, encodage)
* Exécuter l’algorithme de Gradient Descent pour la régression linéaire et la classification logistique
* Ajuster visuellement les hyperparamètres (learning rate α, nombre d’itérations)
* Observer en temps réel la convergence via la learning curve et mesurer la performance

---

## 🔥 Fonctionnalités

| 🚩 # | Module                                           |  ✅ Statut       |
| ---- | ------------------------------------------------ | ------ | -------- |
| 1    | Importer un Dataset (CSV / Excel)                |                   |
| 2    | Dashboard Statistique (mean, median, histo, box) |                   |
| 3    | Prétraitement (imputation, scaling, encodage)    |                   |
| 4    | Implémentation de Gradient Descent               |                   |
| 5    | Affichage des Metrics (MSE, RMSE, accuracy…)     |                   |
| 6    | Contrôles Hyperparamètres & Learning Curve       |                   |
| 7    | Design & UX/UI                                   |                   |


---

## ⚙️ Stack Technique

* **Langage** : Python 3.8+
* **Graphique** : *Choix* entre **Tkinter** (desktop) ou **Django** + Bootstrap & Chart.js (web)
* **Data & ML** :

  * pandas, NumPy
  * scikit‑learn (metrics, helpers)
  * GD codé manuellement pour pédagogie
* **Visualisation** : Matplotlib, Seaborn ou Plotly
* **Versionning** : Git & GitHub
* **Documentation** : Markdown, Poster PDF

---

## 🏗️ Architecture & Conception

```text
┌───────────────────────────┐      ┌─────────────────────────┐
│   Interface Utilisateur   │◄────►│     Contrôleur (API)    │
│ (Tkinter / Django views)  │      │ (Events / AJAX calls)   │
└───────────────────────────┘      └─────────────────────────┘
            │                                 │
            ▼                                 ▼
   ┌───────────────────┐            ┌────────────────────────┐
   │ Data Loader &     │            │ Gradient Descent Core  │
   │ Préprocessing     │            │ (Reg / Clf + α, iter)  │
   └───────────────────┘            └────────────────────────┘
                   \              /
                    \            /
                     ▼          ▼
                ┌─────────────────────┐
                │ Évaluation & Charts │
                │ (Metrics + Curves)  │
                └─────────────────────┘
```

---

## 🔧 Installation & Lancement

```bash
# 1. Cloner ce dépôt
git clone https://github.com/votre-utilisateur/gradient-descent-visualizer.git
cd gradient-descent-visualizer

# 2. Créer et activer un environnement virtuel
python -m venv venv
source venv/bin/activate   # macOS / Linux
venv\Scripts\activate    # Windows

# 3. Installer les dépendances
pip install -r requirements.txt

# 4a. Desktop (Tkinter)
python app.py

# 4b. Web (Django)
cd webapp
python manage.py migrate
python manage.py runserver
```

---

## 🎮 Guide d’Utilisation

1. **Importer** : Cliquez sur **» Charger Dataset »** et sélectionnez votre fichier.
2. **Explorer** : Consultez les statistiques descriptives et graphiques interactifs.
3. **Prétraiter** : Gérez valeurs manquantes, normalisez et encodez.
4. **Exécuter** : Sélectionnez **Régression** ou **Classification**, fixez α et le nombre d’itérations.
5. **Visualiser** : Suivez la convergence de la fonction de coût et l’évolution des metrics.

> 💡 **Astuce** : Testez plusieurs valeurs de α pour comprendre leur impact sur la vitesse de convergence.

---

## 🔍 Paramétrage & Optimisation

* **Learning Rate (α)** : slider de `0.0001` à `1.0` avec pas ajustable
* **Iterations** : slider de `10` à `10 000`
* **Mini‑batch** : (optionnel) taille de batch configurée
* **Courbe d’apprentissage** : tracée en temps réel ou après exécution

---

## 📂 Organisation du Code

```text
gradient-descent-visualizer/
├── data/                  # Exemple de datasets
├── src/
│   ├── loader.py          # Upload & preprocessing
│   ├── gd_core.py         # Implémentation GD
│   ├── metrics.py         # Calcul des performances
│   ├── ui/                # Interface (Tkinter / Django)
│   └── utils.py           # Helpers & utilitaires
├── requirements.txt       # Dépendances Python
├── app.py                 # Entrée desktop (Tkinter)
├── webapp/                # Projet Django (si web)
└── README.md              # Documentation projet
```

---

## 🤝 Contribution & Workflow Git

1. **Fork** ce dépôt
2. `git checkout -b feature/ma-feature`
3. `git commit -m "✨ add nouvelle fonctionnalité"`
4. `git push origin feature/ma-feature`
5. Ouvrez une **Pull Request**

---

## 📜 Licence

Ce projet est distribué sous licence **MIT**. Consultez le fichier [LICENSE](LICENSE) pour plus de détails.
