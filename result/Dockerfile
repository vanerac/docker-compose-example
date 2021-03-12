FROM node:12.21.0-alpine3.12

COPY . /app

WORKDIR /app

RUN npm i

EXPOSE 80

ENV port=80

CMD ["node", "./server.js"]
