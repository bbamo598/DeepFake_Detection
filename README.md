# DeepFake_Detection

Ce projet vise à concevoir un système de détection de vidéos DeepFake en utilisant des techniques de Deep Learning. Il comprend la collecte et le prétraitement de vidéos réelles et truquées, l’extraction de frames, et l’entraînement d’un modèle CNN basé sur transfer learning (InceptionV3 ou ResNet50) avec TensorFlow. Le projet délivrera un MVP fonctionnel capable de détecter des DeepFakes sur un dataset réduit, accompagné d’une première version d’article scientifique présentant la méthodologie, les résultats et les perspectives pour une version finale plus robuste et complète.

# Structure du projet

deepfake_project/
│
├─ data/                    Vidéos brutes (réelles et truquées)
│   ├─ raw/
│   │   ├─ real/            Vidéos réelles
│   │   └─ fake/            Vidéos DeepFake
│   └─ processed/            Frames extraites et prétraitées
│       ├─ train/
│       │   ├─ real/
│       │   └─ fake/
│       ├─ validation/
│       │   ├─ real/
│       │   └─ fake/
│       └─ test/
│           ├─ real/
│           └─ fake/
│
├─ notebooks/               Notebooks Jupyter pour expérimentation
│   ├─ data_preprocessing.ipynb
│   ├─ model_training.ipynb
│   └─ evaluation.ipynb
│
├─ scripts/                 Scripts Python modulaires
│   ├─ extract_frames.py
│   ├─ preprocess_frames.py
│   ├─ train_model.py
│   ├─ evaluate_model.py
│   └─ utils.py              Fonctions utilitaires (extraction, métriques, etc.)
│
├─ models/                  Modèles sauvegardés
│   ├─ mvp_model.h5
│   └─ final_model.h5
│
├─ results/                 Résultats du modèle et graphiques
│   ├─ metrics/             Tables de performance
│   └─ plots/               Courbes ROC, graphiques d’analyse
│
├─ docs/                    Documentation et article scientifique
│   ├─ article_mvp.docx
│   └─ article_final.docx
│
├─ requirements.txt         Dépendances Python
└─ README.md                Présentation générale du projet


data/raw : stocke les vidéos originales (réelles et truquées).
data/processed : contient les frames extraites et préparées pour l’entraînement.
notebooks/ : pour l’expérimentation interactive et les tests rapides.
scripts/ : scripts modulaires pour automatiser extraction, prétraitement, entraînement et évaluation.
models/ : sauvegarde les modèles entraînés (MVP et final).
results/ : pour stocker métriques et visualisations qui serviront dans l’article.
docs/ : article scientifique et autres documents du projet.
requirements.txt : toutes les bibliothèques Python nécessaires pour reproduire le projet.
README.md : description générale, instructions d’installation et d’exécution.
