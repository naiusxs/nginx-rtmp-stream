# Utilizar imagen base con Nginx y RTMP
FROM tiangolo/nginx-rtmp

# Copiar la configuración personalizada de Nginx
COPY nginx.conf /etc/nginx/nginx.conf

# Copiar los archivos HTML a la ruta donde Nginx puede servirlos
COPY public /usr/share/nginx/html

# Instalar herramientas necesarias para acceso remoto (bash y otras)
RUN apt-get update && apt-get install -y bash curl vim

# Exponer los puertos necesarios para HTTP y RTMP
EXPOSE 80 1935

# Comando por defecto que mantiene el contenedor activo (temporal para pruebas)
CMD ["tail", "-f", "/dev/null"]

# Si quieres iniciar Nginx automáticamente para producción, usa este comando en su lugar:
# CMD ["nginx", "-g", "daemon off;"]
