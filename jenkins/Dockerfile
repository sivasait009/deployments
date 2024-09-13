# Use the official Node.js image.
FROM node:14

# Create and change to the app directory.
WORKDIR /usr/src/app

# Copy application dependency manifests to the container image.
COPY package*.json ./

# Install production dependencies.
RUN npm install --only=production

# Copy the source code into the container.
COPY . .

# Run the web service on container startup.
CMD [ "npm", "start" ]

# Document that the service listens on port 3000.
EXPOSE 3000
