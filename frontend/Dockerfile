FROM node:16-alpine AS base

WORKDIR /app

ADD package.json .
RUN npm i

COPY . .

EXPOSE 3000

CMD npm start