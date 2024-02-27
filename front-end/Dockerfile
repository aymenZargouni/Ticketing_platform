# Step 1: Node.js base image
FROM node:latest as builder

WORKDIR /app

# Copy the rest of your application code
COPY . .

# Step 2: Nginx setup
FROM nginx:alpine

# Copy built assets from builder stage
COPY --from=builder /app/dist/* /usr/share/nginx/html/

# Optional: Copy custom Nginx configuration
COPY src/nginx/etc/conf.d/default.conf /etc/nginx/conf.d/
