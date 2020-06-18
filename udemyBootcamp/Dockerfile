FROM node:alpine

ARG NODE_ENV=development
ENV NODE_ENV $NODE_ENV

ARG PORT=3000
ENV PORT $PORT
EXPOSE $PORT

RUN npm i -g npm@latest



WORKDIR /usr/src/node

COPY package*.json ./

RUN npm i -f

ENV PATH /usr/src/node/node_modules/.bin:$PATH

WORKDIR /usr/src/node/app
COPY . .


CMD ["node","app.js"]