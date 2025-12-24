# Use an official Node.js runtime as a parent image
FROM node:18-alpine

# Set working directory inside the container
WORKDIR /app

# Copy only package.json and package-lock.json first (caching dependencies)
COPY package*.json ./
rm -rf node_modules package-lock.json

# Install app dependencies
RUN npm install

# Copy the rest of the application code
COPY . .

# Expose the port your Express app runs on
EXPOSE 3001

# Run the app
CMD ["node", "appointment-service.js"]
