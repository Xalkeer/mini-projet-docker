# Étape 1 : image Python
FROM python:3.11-slim

# Étape 2 : définir le répertoire de travail
WORKDIR /app

# Étape 3 : copier le contenu du dossier vote dans le conteneur
COPY vote/ /app/

# Étape 4 : installer les dépendances
RUN pip install --no-cache-dir -r requirements.txt

# Étape 5 : exposer le port utilisé par ton app
EXPOSE 8080

# Étape 6 : lancer l'application
CMD ["python", "app.py"]
