FROM node:16-alpine

WORKDIR /usr/app

COPY entrypoint.sh /entrypoint.sh
RUN chmod +x /entrypoint.sh

COPY package.json ./

ENTRYPOINT ["/entrypoint.sh"]

RUN npm install
COPY . .
EXPOSE 8080

CMD ["npm", "run", "dev"]