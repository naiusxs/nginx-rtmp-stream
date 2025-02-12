# Utilizar imagen base con Nginx y RTMP
FROM tiangolo/nginx-rtmp

# Copiar la configuración personalizada de Nginx
COPY nginx.conf /etc/nginx/nginx.conf

# Copiar los archivos HTML a la ruta correcta
COPY public /usr/local/nginx/html

# Instalar herramientas necesarias
RUN apt-get update && apt-get install -y nginx bash curl vim

# Exponer los puertos HTTP (80) y RTMP (1935)
EXPOSE 80 1935

# Mantener el contenedor activo para debug (opción temporal)
CMD ["tail", "-f", "/dev/null"]

# Para producción, descomenta la siguiente línea:
CMD ["nginx", "-g", "daemon off;"]
