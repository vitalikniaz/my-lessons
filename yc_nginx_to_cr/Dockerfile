# Pull the minimal Ubuntu image
FROM ubuntu

# Install Nginx
RUN apt-get -y update && apt-get -y install nginx

# Copy the Nginx config
COPY default.cfg /etc/nginx/sites-available/default.cfg

# Expose the port for access
EXPOSE 80/tcp

# Run the Nginx server
CMD ["/usr/sbin/nginx", "-g", "daemon off;"]