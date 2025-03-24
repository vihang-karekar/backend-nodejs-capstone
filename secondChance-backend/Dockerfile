FROM node:18.12.1-bullseye-slim

WORKDIR /usr/src/app

COPY package*.json ./

RUN npm install

COPY . .

RUN cd util/import-mongo && node index.js && cd ../..

EXPOSE 3060

CMD ["node", "app.js"]