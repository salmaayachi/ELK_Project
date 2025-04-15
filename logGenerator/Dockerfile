# Utiliser une image de base Python
FROM python:3.9-slim

# Créer un répertoire dans l'image pour stocker l'application
WORKDIR /usr/src/app

# Copier le script Python dans le conteneur
COPY generate_logs.py .

# Installer les dépendances Python nécessaires (si tu en as)
# RUN pip install -r requirements.txt  # Si tu veux ajouter des dépendances

# Commande pour démarrer l'application Python
CMD ["python", "generate_logs.py"]
