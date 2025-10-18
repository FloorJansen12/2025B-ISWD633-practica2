# COMPLETAR  
Comparando sus conocimientos antes de hacer la práctica con sus conocimientos después de hacer la tarea, explicar los principales aprendizajes logrados para beneficio de su formación profesional.  
Si solucionó un problema presentado al realizar la práctica también se debe documentar.

- Antes de la práctica tenía conocimientos básicos sobre Docker, pero no sabía bien cómo gestionar configuraciones internas. Durante esta práctica aprendí a crear contenedores usando variables de entorno de manera manual. Además, el uso de redes personalizadas para conectar contenedores y organizar mejor los servicios, que en este caso utilizamos Bridge para todos. Un problema que encontré fue al ejecutar MySQL, por no definir variables como MYSQL_ROOT_PASSWORD. Al solucionarlo entendí la importancia de las configuraciones correctas.

Consultar: Cómo se gestionan datos confidenciales con los secretos de Docker (Docker Secrets).

- Los Docker Secrets permiten gestionar datos confidenciales (como contraseñas, claves o certificados) de forma segura dentro de contenedores. En lugar de almacenar esta información en variables de entorno o archivos dentro de la imagen, los secretos se guardan encriptados en el manager del clúster Docker Swarm.
