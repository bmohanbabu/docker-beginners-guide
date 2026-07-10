# Base image
FROM node:18-alpine

# Set working directory inside container
WORKDIR /app

# Copy package files first (for better layer caching)
COPY package.json .

# Install dependencies
RUN npm install

# Copy rest of the application code
COPY . .

# Document the port the app uses
EXPOSE 3000

# Command to run the app
CMD ["npm", "start"]
