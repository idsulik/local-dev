FROM node:18-bullseye-slim

WORKDIR /app

COPY web/package*.json ./

RUN npm install

COPY web/ ./

EXPOSE 3000

CMD ["npm", "start"]