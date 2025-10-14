### Crear contenedor de Postgres sin que exponga los puertos. Usar la imagen: postgres:15-alpine3.21

```
docker run -d --name postgres -e POSTGRES_PASSWORD=bernibd postgres:15-alpine3.21
```

### Crear un cliente de postgres. Usar la imagen: dpage/pgadmin4

```
docker run -d --name pgadmin -e PGADMIN_DEFAULT_EMAIL=admin@admin.com -e PGADMIN_DEFAULT_PASSWORD=admin -p 8080:80 dpage/pgadmin4
```

# COMPLETAR

La figura presenta el esquema creado en donde los puertos son:
- a: (completar con el valor)
- b: (completar con el valor)
- c: (completar con el valor)

![Imagen](esquema-2-ejercicio.PNG)

## Desde el cliente
### Acceder desde el cliente al servidor postgres creado.

<img width="1919" height="910" alt="image" src="https://github.com/user-attachments/assets/e62ae04b-8e02-4a22-a593-70477bfc70f4" />

<img width="1919" height="921" alt="image" src="https://github.com/user-attachments/assets/a5ffe464-cf91-41bd-a2a0-2f43b40f3b74" />


# COMPLETAR CON UNA CAPTURA DEL LOGIN
### Crear la base de datos info, y dentro de esa base la tabla personas, con id (serial) y nombre (varchar), agregar un par de registros en la tabla, obligatorio incluir su nombre.

```

docker exec -it postgres psql -U postgres

postgres-# \c Info

CREATE TABLE personas (
    id SERIAL PRIMARY KEY,
    nombre VARCHAR(50)
);

INSERT INTO personas (nombre) VALUES ('Jhordy');
INSERT INTO personas (nombre) VALUES ('SnowPoom');
INSERT INTO personas (nombre) VALUES ('Chestcito');
INSERT INTO personas (nombre) VALUES ('LeoKaiser');
INSERT INTO personas (nombre) VALUES ('Chispitas');
INSERT INTO personas (nombre) VALUES ('Toñito');
INSERT INTO personas (nombre) VALUES ('PixxiePayasita');
INSERT INTO personas (nombre) VALUES ('Adnux');
```

## Desde el servidor postgresl
### Acceder al servidor
### Conectarse a la base de datos info
# COMPLETAR
### Realizar un select *from personas

<img width="897" height="757" alt="image" src="https://github.com/user-attachments/assets/95df6a82-361f-4c8c-b29f-371d34ee92f9" />

# AGREGAR UNA CAPTURA DE PANTALLA DEL RESULTADO
