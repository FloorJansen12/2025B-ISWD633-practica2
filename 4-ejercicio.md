## Esquema para el ejercicio
![Imagen](esquema-4-ejercicio.PNG)

### Crear la red

```
docker network create net-wp -d bridge
```

# COMPLETAR

### Crear el contenedor mysql a partir de la imagen mysql:8, configurar las variables de entorno necesarias

```
docker run --name mysql --network net-wp -e MYSQL_ROOT_PASSWORD=bernibd -e MYSQL_DATABASE=mysql -d mysql:8
```

# COMPLETAR

### Crear el contenedor wordpress a partir de la imagen: wordpress, configurar las variables de entorno necesarias

```
docker run --name wordpress --network net-wp -p 8787:80 -e WORDPRESS_DB_HOST=mysql -e WORDPRESS_DB_USER=root -e WORDPRESS_DB_PASSWORD=bernibd -e WORDPRESS_DB_NAME=mysql -d wordpress
```

# COMPLETAR

De acuerdo con el trabajo realizado, en el esquema del ejercicio el puerto a es 8787

Ingresar desde el navegador al wordpress y finalizar la configuración de instalación.

<img width="1731" height="1556" alt="image" src="https://github.com/user-attachments/assets/625474c3-b3fc-4d49-9646-8ab8fa8bd2e7" />

# COLOCAR UNA CAPTURA DE LA CONFIGURACIÓN

Desde el panel de admin: cambiar el tema y crear una nueva publicación.
Ingresar a: http://localhost:9300/ 
recordar que a es el puerto que usó para el mapeo con wordpress
# COLOCAR UNA CAPTURA DEL SITO EN DONDE SEA VISIBLE LA PUBLICACIÓN.

### Eliminar el contenedor wordpress
# COMPLETAR

### Crear nuevamente el contenedor wordpress
Ingresar a: http://localhost:9300/ 
recordar que a es el puerto que usó para el mapeo con wordpress

### ¿Qué ha sucedido, qué puede observar?
# COMPLETAR

