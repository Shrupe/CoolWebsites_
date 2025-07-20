# Stage 1: Build
FROM node:20-alpine AS builder

WORKDIR /app

# Copy only package files first for better caching
COPY package.json package-lock.json ./

# Install dependencies
RUN npm install

# Copy the rest of the project
COPY . .

# Build the frontend (output goes to /app/dist)
RUN npm run build

# Stage 2: Serve using Nginx
FROM nginx:stable-alpine

# Copy built files from the builder stage
COPY --from=builder /app/dist /usr/share/nginx/html

# Replace default nginx config
COPY nginx.conf /etc/nginx/conf.d/default.conf

# Expose port (for debugging)
EXPOSE 80

