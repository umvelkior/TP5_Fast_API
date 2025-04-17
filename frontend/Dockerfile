FROM node:22

USER root
WORKDIR /home/node/app

# Copie les fichiers, puis change les permissions
COPY package*.json ./
RUN chown -R node:node /home/node/app

USER node
RUN npm install

COPY --chown=node:node . .

EXPOSE 3000
CMD ["npm", "run", "dev"]
