
FROM node:latest as builder

WORKDIR /app


COPY . .

# Step 2: Nginx setup
FROM nginx:alpine


COPY --from=builder /app/dist/* /usr/share/nginx/html/


COPY src/nginx/etc/conf.d/default.conf /etc/nginx/conf.d/
