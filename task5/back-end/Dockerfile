# Usar la última imagen de Ubuntu
FROM ubuntu:latest

# Actualizar APT
RUN apt-get update

# Instalar software
RUN apt-get upgrade -y

# Instalar Python3 y pip3
RUN apt-get install -y python3 python3-pip

# Eliminar la restricción de gestión externa si existe
RUN rm -f /usr/lib/python*/EXTERNALLY-MANAGED

# Instalar Flask usando pip3
RUN pip3 install flask flask-cors

# Establecer directorio de trabajo
WORKDIR /app

# Copiar la aplicación Flask
COPY ./api.py /app/api.py

# Comando para ejecutar la aplicación Flask
CMD ["python3", "api.py"]