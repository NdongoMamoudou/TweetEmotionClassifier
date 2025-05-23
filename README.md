# TweetEmotionClassifier



# TweetEmotionClassifier

Ce projet Deep Learning vise à construire un modèle Transformer capable de classer les émotions exprimées dans des tweets. Il s'agit d'un classificateur multi-classes entraîné sur un jeu de données fictif appelé **EmoNet**, contenant des tweets annotés selon quatre émotions : **joie**, **tristesse**, **colère**, et **peur**.

## 📌 Objectif

Utiliser un modèle Transformer (architecture de type BERT simplifiée) pour analyser du texte et identifier l'émotion dominante dans des tweets.

---

## 🧠 Modèle

Le modèle utilisé est un Transformer personnalisé construit avec TensorFlow/Keras :
- Tokenization des textes
- Embedding
- Couches de self-attention multi-têtes
- Normalisation et feedforward
- Classification via softmax

Il a été entraîné pendant 3 époques avec les résultats suivants :

| Epoch | Accuracy (train) | Accuracy (val) | Loss (val) |
|-------|------------------|----------------|-------------|
| 1     | 29.2%            | 34.7%          | 1.56        |
| 2     | 58.0%            | 80.3%          | 0.55        |
| 3     | 87.5%            | 89.8%          | 0.26        |

---

## 📂 Structure du projet

```bash
emotion_transformer_project/
│
├── data/                     # Contient le dataset (EmoNet)
├── model/                    # Fichier pour sauvegarde du modèle
├── train.py                  # Script principal d'entraînement
├── predict.py                # Script de prédiction sur nouveau tweet
├── requirements.txt          # Dépendances du projet
└── README.md                 # Description du projet
```

---

## ▶️ Installation

```bash
git clone https://github.com/NdongoMamoudou/TweetEmotionClassifier.git
cd TweetEmotionClassifier
python -m venv env
source env/bin/activate  # ou env\Scriptsctivate sous Windows
pip install -r requirements.txt
```

---

## 🚀 Lancement

### Entraînement du modèle :

```bash
python train.py
```

### Prédiction sur un tweet :

```bash
python predict.py "I'm feeling very happy today!"
```

---

## 📦 requirements.txt (extrait)

```txt
tensorflow
numpy
scikit-learn
matplotlib
transformers
datasets
```

> ⚠️ Si vous utilisez `gym` ou `Box2D` pour d'autres projets, n'oubliez pas d’installer aussi les outils de compilation C++ via Microsoft Build Tools.

---

## 👥 Auteurs

- Ndongo Mamoudou
- Projet encadré dans le cadre du cours de Deep Learning (5e année IPPSSI)

---

## 📬 Contact

Pour toute question, merci de contacter [Ndongo Mamoudou](https://github.com/NdongoMamoudou) via GitHub.

---

## 📜 Licence

Ce projet est distribué sous licence **MIT** – Voir le fichier `LICENSE` pour plus d'informations.
