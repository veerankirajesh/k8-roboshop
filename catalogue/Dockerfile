FROM node:18.20.8-alpine3.21
EXPOSE 8080
RUN addgroup -S roboshop && adduser -S roboshop -G roboshop
WORKDIR /opt/server
RUN chown -R roboshop:roboshop /opt/server
USER roboshop
COPY package.json package-lock.json /opt/server/
RUN npm install
COPY . /opt/server/
CMD ["node", "server.js"]
