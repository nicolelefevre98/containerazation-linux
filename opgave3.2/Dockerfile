# Vælg Node.js som base image
FROM node:alpine

# Sæt arbejdsdirectory
WORKDIR /app

# Kopier package.json og package-lock.json filer
COPY package.json ./
COPY package-lock.json ./

# Installer afhængigheder
RUN npm install

# Kopier resten af applikationskoden
COPY . .

# Byg Strapi projektet
RUN npm run build

# Eksponer den nødvendige port
EXPOSE 1337

# Kør Strapi
CMD ["npm", "start"]
