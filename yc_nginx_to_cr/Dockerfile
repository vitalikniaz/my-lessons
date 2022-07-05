# Pull the minimal Ubuntu image
FROM ubuntu:20.04

# LABEL about the custom image
LABEL maintainer="vitali.kniaz@revolver.by"
LABEL version="0.1"
LABEL description="This is custom Docker Image for tests."

# Disable Prompt During Packages Installation
ARG DEBIAN_FRONTEND=noninteractive

# Update Ubuntu Software repository
RUN apt-get -y update
RUN apt-get -y install nginx

# Copy the Nginx config
COPY default /etc/nginx/sites-available/default

# Expose the port for access
EXPOSE 80/tcp
EXPOSE 8080/tcp
EXPOSE 443/tcp

# Run the Nginx server
CMD ["/usr/sbin/nginx", "-g", "daemon off;"]