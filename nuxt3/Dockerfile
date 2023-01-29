FROM node:18-bullseye-slim

WORKDIR /home/node/app
RUN mkdir -p /home/node/app/node_modules
RUN chown -R node:node /home/node/app
COPY --chown=node:node .npmrc /home/node/app
COPY --chown=node:node package.json /home/node/app
# RUN npm config set unsafe-perm true
# RUN npm install nuxt
RUN npm install --force
# RUN npm install
EXPOSE 3000

CMD ["npm", "run", "dev"]
