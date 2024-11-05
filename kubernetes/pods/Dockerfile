# Download UBUNTU
FROM ubuntu

# Update the system
RUN apt-get update

# In some Linux versions, it’s necessary to set a TIMEZONE variable
ENV TZ=Europe/Madrid

# Then create a file called /etc/timezone to configure it
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

# Install NGINX
RUN apt-get install -y nginx

# Create an index.html file in the default nginx directory
RUN echo 'Example of POD with KUBERNETES and YAML' > /var/www/html/index.html

# Start NGINX through ENTRYPOINT so it cannot be modified when creating the container
ENTRYPOINT ["/usr/sbin/nginx", "-g", "daemon off;"]

# Expose Port 80
EXPOSE 80