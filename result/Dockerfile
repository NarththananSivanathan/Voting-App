# Utilisation de l'image Node.js officielle
FROM node:18

# Définir le répertoire de travail
WORKDIR /app

# Copier package.json et package-lock.json
COPY package.json ./

# Installer les dépendances
RUN npm install

# Copier tout le code source
COPY . .

# Exposer le port de l'application
EXPOSE 8081

# Démarrer l'application
CMD ["node", "server.js"]
