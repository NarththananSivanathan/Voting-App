# Utilisation d'une image de base légère avec Python 3.11
FROM python:3.11-slim

# Définir le répertoire de travail dans le conteneur
WORKDIR /app

# Copier les fichiers nécessaires
COPY requirements.txt .

# Installer les dépendances Python
RUN pip install --no-cache-dir -r requirements.txt

# Copier le reste du code source
COPY . .

# Exposer le port sur lequel l'application écoute
EXPOSE 8080

# Définir la commande pour démarrer l'application
CMD ["python", "app.py"]