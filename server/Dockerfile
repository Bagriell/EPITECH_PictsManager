FROM node:14.19.1-alpine as picsServer

WORKDIR /server

COPY . .

RUN npm install

EXPOSE 8080

ENV WAIT_VERSION 2.7.2
ADD https://github.com/ufoscout/docker-compose-wait/releases/download/$WAIT_VERSION/wait /wait
RUN chmod +x /wait

CMD ["npm", "run", "start"]