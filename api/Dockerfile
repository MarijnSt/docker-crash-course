# Parent layer
FROM node:17-alpine

# Nodemon globaal installeren (hot reloading during dev)
RUN npm install -g nodemon

# Working directory (when we run commands or specify paths, it's from this location)
WORKDIR /app

# Copy dependencies first
COPY package.json .

# Commands that should be run during build (will be run in working directory)
RUN npm install

# Source code layer (copies all files in current folder into the app folder in the image)
COPY . .

# Which port should be exposed from container (used by docker desktop for port mapping)
EXPOSE 4000

# Commands that should be run in runtime (when container is running)
CMD ["npm", "run", "dev"]