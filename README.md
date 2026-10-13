# 🎮 Game Match

**Application web de recommandation comparée de jeux vidéo**

Projet réalisé dans le cadre de la SAE du BUT 3 Informatique à l'IUT de Villetaneuse — Université Sorbonne Paris Nord.

## 📌 Présentation

Game Match est une application web permettant aux utilisateurs de découvrir des jeux vidéo similaires à leurs jeux préférés.

L'objectif principal est de comparer deux méthodes de recommandation afin d'évaluer la pertinence des résultats, les performances algorithmiques et les ressources consommées.

L'application repose sur une architecture découplée séparant le frontend et le backend.

## 🚀 Fonctionnalités prévues

- Recherche et sélection d'un jeu vidéo
- Recommandations basées sur la similarité de Jaccard
- Recommandations basées sur les embeddings sémantiques
- Comparaison des résultats des deux algorithmes
- Affichage des scores de similarité
- Visualisation des performances sous forme de graphiques
- Analyse du temps d'exécution et de la consommation mémoire
- Estimation de l'impact énergétique

## 🛠️ Technologies utilisées

| Composant | Technologies |
|---|---|
| Frontend | Vue.js 3, Vite, JavaScript |
| Backend | Python, FastAPI |
| Base de données | SQLite, SQLAlchemy |
| Traitement des données | Pandas, NumPy |
| Intelligence artificielle | Sentence Transformers |
| Visualisation | Chart.js |
| Tests | Pytest, Vitest |
| Déploiement | Docker |

## 🧠 Méthodes de recommandation

### 1. Similarité de Jaccard

Cette méthode compare les tags associés aux jeux vidéo.

Elle calcule le rapport entre le nombre de tags communs et le nombre total de tags distincts.

**Formule :**

J(A,B) = |A ∩ B| / |A ∪ B|

### 2. Embeddings sémantiques

Cette méthode analyse les descriptions textuelles des jeux vidéo à l'aide du modèle `all-MiniLM-L6-v2` de Sentence Transformers.

Les descriptions sont transformées en vecteurs numériques puis comparées à l'aide de la similarité cosinus.

## 📂 Structure prévue du projet

```text
game-match/
├── backend/
│   ├── main.py
│   ├── controllers/
│   ├── services/
│   └── models/
├── frontend/
│   └── src/
├── data/
├── tests/
├── README.md
└── .gitignore
```

Cette structure est indicative et pourra évoluer pendant le développement.

## ⚙️ Installation et lancement

### Cloner le dépôt

```bash
git clone https://github.com/mohamedflifel/game-match.git
cd game-match
```

### Backend

```bash
cd backend
python -m venv .venv
```

Sous Windows :

```bash
.venv\Scripts\activate
```

Installer les dépendances initiales :

```bash
pip install fastapi uvicorn
```

Lancer le serveur :

```bash
uvicorn main:app --reload
```

API accessible sur `http://127.0.0.1:8000`

### Frontend

Dans un deuxième terminal :

```bash
cd frontend
npm install
npm run dev
```

Frontend accessible à l'adresse indiquée par Vite, généralement `http://localhost:5173`.

Ces instructions correspondent à la configuration initiale du projet et seront mises à jour au fur et à mesure du développement.

## 👥 Équipe — Les Castors bâtisseurs

- Kenzo Fillonneau
- Tristan Collen
- Elaa Maiz
- Amira Ben Chaabane
- Mohamed Flifel

## 🌿 Organisation Git

Chaque membre travaille sur sa propre branche selon la convention :

`prenom/version`

Les modifications seront intégrées à la branche principale après vérification.

## 📊 Dataset

Le dataset de jeux vidéo sera sélectionné sur Kaggle.

Les critères de sélection sont la présence de tags, de descriptions textuelles, la qualité des données et les conditions de licence.

La source, l'auteur et la licence du dataset seront ajoutés après sa sélection.

## 📈 Évaluation des performances

Les deux approches seront comparées selon :

- La qualité des recommandations
- Le temps d'exécution
- La consommation mémoire
- La complexité algorithmique
- L'impact énergétique estimé

## 📜 Licence

Le code source du projet est destiné à être distribué sous licence MIT.

La licence du dataset sera vérifiée séparément.

## 🚧 État du projet

**En cours de développement**

Les premières étapes concernent la mise en place de l'environnement, la communication frontend/backend et la sélection du dataset.
