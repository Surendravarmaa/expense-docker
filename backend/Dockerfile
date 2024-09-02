FROM node:20
EXPOSE 8080
# Install shadow package to get useradd command
RUN apk add --no-cache shadow
RUN useradd expense
RUN mkdir /opt/server
RUN chown expense:expense -R /opt/server
WORKDIR /opt/server
COPY package.json .
COPY *.js .
RUN npm install
CMD ["node","index.js"]

