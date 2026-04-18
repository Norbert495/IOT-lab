FROM node:24.15.0-alpine3.22

WORKDIR /usr/src/app

COPY package*.json ./

RUN npm install && npm install -g nodemon

COPY . .

EXPOSE 3000

CMD ["nodemon", "-L", "src/index.js"]