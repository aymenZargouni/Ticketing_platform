
FROM node:latest as builder

WORKDIR /app

<<<<<<< HEAD

COPY . .


=======
# Copy the rest of your application code
COPY . .

# Step 2: Nginx setup
>>>>>>> 4cdaa995de1322af04278c940839757e605fd61b
FROM nginx:alpine


COPY --from=builder /app/dist/* /usr/share/nginx/html/


COPY src/nginx/etc/conf.d/default.conf /etc/nginx/conf.d/
