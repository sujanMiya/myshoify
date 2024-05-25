# docker/nginx/Dockerfile
FROM nginx:alpine

# Copy custom configuration file from the current directory
COPY default.conf /etc/nginx/conf.d/default.conf

# Remove default server definition
RUN rm /etc/nginx/conf.d/default.conf

# Copy over our custom config
COPY ./default.conf /etc/nginx/conf.d/

EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
