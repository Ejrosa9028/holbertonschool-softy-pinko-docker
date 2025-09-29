# Usar la última imagen de Nginx
FROM nginx:latest

# Copiar los archivos del front-end al directorio de Nginx
COPY ./softy-pinko-front-end /var/www/html/softy-pinko-front-end

# Copiar la configuración personalizada de Nginx
COPY ./softy-pinko-front-end.conf /etc/nginx/conf.d/default.conf

# Exponer el puerto 9000
EXPOSE 9000

# Iniciar Nginx en primer plano
CMD ["nginx", "-g", "daemon off;"]