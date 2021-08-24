FROM node:alpine

WORKDIR /usr/app

COPY ./package.json ./
RUN npm instal
COPY . .

CMD ["npm", "run" ,"start"]