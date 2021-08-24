FROM node:alpine

WORKDIR /usr/app

COPY ./package.json ./
RUN npm instal
COPY . .

EXPOSE 5000
CMD ["npm", "run" ,"start"]