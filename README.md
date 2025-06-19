# MLOPS-LungCancer - README.md (Instructions)

## 🔧 Installation
```bash
pip install bentoml tensorflow
```

## 📦 Sauvegarde du modèle (déjà fourni)
Place `model_resnet50_cancer_20250528_163309 (2).h5` dans le dossier du projet.

## 🚀 Construction du service Bento
```bash
python service.py     # Sauvegarde le modèle dans le store BentoML
bentoml build          # Crée le bento
bentoml containerize cancer_classifier:latest  # Image Docker prête à déployer
```

## 🐳 Déploiement (Docker)
```bash
docker run -it --rm -p 3000:3000 cancer_classifier:latest
```

Accède à la doc interactive ici : [http://localhost:3000/docs](http://localhost:3000/docs)
