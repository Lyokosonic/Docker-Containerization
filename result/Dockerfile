FROM node:10

RUN mkdir -p /usr/src/result/

WORKDIR /usr/src/result

COPY package*.json /usr/src/result/

RUN npm install

COPY . /usr/src/result/

EXPOSE 80

CMD [ "npm", "start" ]
