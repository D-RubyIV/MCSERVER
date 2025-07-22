FROM node:18-alpine AS build

FROM node:18-alpine

WORKDIR /app

RUN npm install -g http-server

CMD ["http-server", "-p", "3000"]