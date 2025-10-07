# Variables de Entorno
### ¿Qué son las variables de entorno?

Son variables dinámicas que son utilizadas por el sistema operativo y algunos programas para su correcto funcionamiento, sin la necesidad de incluirlas directamente en el programa.

### Para crear un contenedor con variables de entorno

```
docker run -d --name <nombre contenedor> -e <nombre variable1>=<valor1> -e <nombre variable2>=<valor2>
```

### Crear un contenedor a partir de la imagen de nginx:alpine con las siguientes variables de entorno: username y role. Para la variable de entorno rol asignar el valor admin.

```
docker run -d --name holadios -e username=Diablo -e role=admin nginx:alpine
```

<img width="897" height="374" alt="image" src="https://github.com/user-attachments/assets/140407ec-d91e-4c30-9671-86638ead5477" />

### Crear un contenedor con la imagen de mysql, mapear todos los puertos

```
docker run -d -P --name berni mysql:latest
```

### ¿El contenedor se está ejecutando?

No se está ejecutando

### Identificar el problema

La base de datos no está inicializada y además, las variables de entorno no están especificadas.

You need to specify one of the following as an environment variable:

    - MYSQL_ROOT_PASSWORD
    
    - MYSQL_ALLOW_EMPTY_PASSWORD
    
    - MYSQL_RANDOM_ROOT_PASSWORD

### Para crear un contenedor con variables de entorno especificadas
- Portabilidad: Las aplicaciones se vuelven más portátiles y pueden ser desplegadas en diferentes entornos (desarrollo, pruebas, producción) simplemente cambiando el archivo de variables de entorno.
- Centralización: Todas las configuraciones importantes se centralizan en un solo lugar, lo que facilita la gestión y auditoría de las configuraciones.
- Consistencia: Asegura que todos los miembros del equipo de desarrollo o los entornos de despliegue utilicen las mismas configuraciones.
- Evitar Exposición en el Código: Mantener variables sensibles como contraseñas, claves API, y tokens fuera del código fuente reduce el riesgo de exposición accidental a través del control de versiones.
- Control de Acceso: Los archivos de variables de entorno pueden ser gestionados con permisos específicos, limitando quién puede ver o modificar la configuración sensible.

### Crear un contenedor con mysql, mapear todos los puertos y configurar las variables de entorno mediante un archivo
# COMPLETAR


<img width="2082" height="731" alt="image" src="https://github.com/user-attachments/assets/1e319b83-4030-4177-b2d1-c74304559915" />


# CAPTURA CON LA COMPROBACIÓN DE LA CREACIÓN DE LAS VARIABLES DE ENTORNO DEL CONTENEDOR ANTERIOR 

### ¿Qué bases de datos existen en el contenedor creado?

mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| performance_schema |
| sys                |
+--------------------+
4 rows in set (0.001 sec)


# COMPLETAR
