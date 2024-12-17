# Search a base image
FROM nginx:latest

# Copy the file into another folder
COPY softy-pinko-front-end /var/www/html/softy-pinko-front-end

# Copy the file into another folder
COPY ./softy-pinko-front-end.conf /etc/nginx/conf.d/default.conf

# Open a port
EXPOSE 9000

# Launch the container with these parameters
CMD ["nginx", "-g", "daemon off;"]
