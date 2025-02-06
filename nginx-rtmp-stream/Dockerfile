FROM tiangolo/nginx-rtmp

# Copiar la configuración de Nginx
COPY nginx.conf /etc/nginx/nginx.conf

# Copiar los archivos HTML a la ruta donde Nginx los puede servir
COPY public /usr/share/nginx/html

# Instalar bash (opcional, si es necesario para el shell interactivo)
RUN apt-get update && apt-get install -y bash

# Mantener el contenedor activo para debug (solo temporal)
CMD ["tail", "-f", "/dev/null"]

# Comando para producción (puedes usar esto en lugar del comando anterior)
# CMD ["nginx", "-g", "daemon off;"]

