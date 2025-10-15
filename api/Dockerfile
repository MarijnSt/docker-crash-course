# Parent layer
FROM node:17-alpine

# Working directory (when we run commands or specify paths, it's from this location)
WORKDIR /app

# Source code layer (copies all files in current folder into the app folder in the image)
COPY . .

# Commands that should be run during build (will be run in working directory)
RUN npm install

# Which port should be exposed from container (used by docker desktop for port mapping)
EXPOSE 4000

# Commands that should be run in runtime (when container is running)
CMD ["node", "app.js"]