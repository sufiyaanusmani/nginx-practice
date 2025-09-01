FROM nginx:stable-alpine

# Remove the default nginx configuration and add our own
COPY nginx.conf /etc/nginx/nginx.conf

# Copy static site into the container
COPY site /usr/share/nginx/html

# Expose default HTTP port
EXPOSE 80

CMD ["/usr/sbin/nginx", "-g", "daemon off;"]
