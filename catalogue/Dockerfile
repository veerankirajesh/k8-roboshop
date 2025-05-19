FROM node:18.20.8-alpine3.21
EXPOSE 8080
RUN adduser -S roboshop && adduser -S roboshop -G roboshop
WORKDIR /opt/server
RUN chmod roboshop:roboshop /opt/server
USER roboshop
COPY package.json /opt/server/
COPY server.js /opt/server/
RUN npm install
CMD ["node", "server.js"]