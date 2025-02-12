# Usar la imagen base de Nginx con RTMP
FROM tiangolo/nginx-rtmp

# Copiar la configuración de Nginx
COPY nginx.conf /etc/nginx/nginx.conf

# Copiar los archivos HTML a la ruta donde Nginx puede servirlos
COPY public /usr/share/nginx/html

# Instalar herramientas necesarias para acceso remoto
RUN apt-get update && apt-get install -y bash curl vim

# Asegurar que /bin/bash esté disponible
RUN ln -sf /bin/bash /bin/sh

# Exponer los puertos HTTP y RTMP
EXPOSE 80 1935

# Mantener el contenedor activo para depuración
CMD ["tail", "-f", "/dev/null"]
