# Use Node to build and serve the React app
FROM node:18

WORKDIR /app

# Copy project files
COPY package*.json ./
COPY tsconfig*.json ./
COPY vite.config.* ./
# COPY .env.production .env.production

RUN npm install

COPY . .

# Build the React app
RUN npm run build

# Expose port and use Vite's built-in preview server
EXPOSE 4173
CMD ["npm", "run", "preview"]
