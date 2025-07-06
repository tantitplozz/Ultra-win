# WebUI Dockerfile (Next.js)
FROM node:18-alpine

# Set working directory
WORKDIR /app

# Install dependencies
COPY ../next.js/package.json ./
COPY ../next.js/package-lock.json ./
RUN npm install

# Copy source code
COPY ../next.js/ .

# Build the app
RUN npm run build

# Expose port and start the app
EXPOSE 3000
CMD ["npm", "start"]
