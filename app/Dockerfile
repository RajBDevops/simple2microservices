FROM node:18-alpine

WORKDIR /app

# Copy only dependency files first
COPY package.json package-lock.json ./

# Install ONLY production dependencies
RUN npm ci --omit=dev

# Copy application source code
COPY . .

EXPOSE 3001

CMD ["node", "appointment-service.js"]
