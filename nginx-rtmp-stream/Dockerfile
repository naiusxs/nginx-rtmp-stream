FROM tiangolo/nginx-rtmp

# Copiar la configuración personalizada de Nginx
COPY nginx.conf /etc/nginx/nginx.conf

# Copiar los archivos HTML a la ruta donde Nginx puede servirlos
COPY public /usr/share/nginx/html

# Instalar herramientas necesarias (bash, sh, curl, vim)
RUN apt-get update && apt-get install -y bash curl vim busybox

# Exponer los puertos HTTP y RTMP
EXPOSE 80 1935

# Mantener el contenedor activo para pruebas
CMD ["tail", "-f", "/dev/null"]

# Para producción, descomenta la siguiente línea:
CMD ["nginx", "-g", "daemon off;"]
