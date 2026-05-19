# Use a clean, lightweight official Node image
FROM node:22-alpine

# Create and set the application directory inside the container
WORKDIR /usr/src/app

# Copy dependency structures
COPY package*.json ./

# Install only production dependencies (excluding dev tools like nodemon)
RUN npm install --only=production

# Copy all backend source code into the container
COPY . .

# Inform Docker that the container listens on port 4000
EXPOSE 4000

# Start the application using standard node
CMD ["node", "server.js"]