# Softy Pinko Docker 🐳

Repositorio de proyectos Docker para **Holberton School**.  
Este repo contiene varios ejercicios prácticos para aprender a trabajar con **Docker**, **Docker Compose** y **Nginx** como proxy y balanceador de carga.

---

## 📂 Estructura del repositorio

- **task0/** → Crear una imagen Docker básica basada en `ubuntu:latest` que imprime `Hello, World!`.
- **task1/** → Instala **Python3**, **pip3** y **Flask**, con un servidor Flask en el puerto 5252 que responde `"Hello, World!"`.
- **task5/** → Configuración de 3 servicios con Docker Compose:
  - **front-end** (contenido estático con Nginx)
  - **back-end** (API con Flask en Python)
  - **proxy** (Nginx como proxy inverso que enruta tráfico entre front-end y back-end)
- **task6/** → Extensión de `task5`, agregando **varias instancias del back-end** y utilizando Nginx como **balanceador de carga Round-Robin**.

---

## 🚀 Uso

### 1️⃣ Construir las imágenes
```bash
sudo docker-compose build
```

### 2️⃣ Levantar los servicios
```bash
Copy code
sudo docker-compose up
```
Esto levantará los contenedores definidos en docker-compose.yml.

### 3️⃣ Acceder a la aplicación
Abre en el navegador:

```arduino
Copy code
http://localhost
```

## ⚡ Task6: Escalar el back-end
En task6, la API puede escalarse fácilmente con el flag --scale.

Ejemplo para levantar 2 contenedores back-end:

```bash
Copy code
sudo docker-compose up --scale back-end=2
```
Esto creará:

task6-back-end-1

task6-back-end-2

task6-front-end-1

task6-proxy-1

Cada request se enviará alternadamente entre los back-ends gracias al balanceo Round-Robin de Nginx.

El comando exacto usado para esto se encuentra en:

Copy code
task6/2-api-servers.txt

🛠️ Requisitos
Docker ≥ 20.10

Docker Compose (paquete docker-compose-plugin o el binario clásico)

✨ Autor
Emanuel Rosa Alamo
Proyecto realizado como parte del programa Holberton School.
Repositorio: holbertonschool-softy-pinko-docker
