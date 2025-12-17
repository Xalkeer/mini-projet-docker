# Étape 1 : image Node officielle
FROM node:20-alpine

# Dossier de travail dans le conteneur
WORKDIR /app

# Copier package.json et package-lock.json DEPUIS LE CONTEXT
COPY result/package.json result/package-lock.json ./

# Installer les dépendances
RUN npm install

# Copier le reste du code Node
COPY result/ .

# Exposer le port
EXPOSE 3000

# Lancer l'application
CMD ["npm", "start"]
