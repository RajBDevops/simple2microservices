FROM node:18-alpine

WORKDIR /app

COPY app/package*.json ./
RUN npm ci

COPY app/ .

CMD ["node", "appointment-service.js"]
