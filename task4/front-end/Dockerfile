# Start your image with an nginx base image
FROM nginx:latest

# Paste files from front-end in nginx folder
COPY ./softy-pinko-front-end /var/www/html/softy-pinko-front-end

# Paste config Nginx file
COPY ./softy-pinko-front-end.conf /etc/nginx/conf.d/default.conf

# Expose Port 9000
EXPOSE 9000
