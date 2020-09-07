## Contenedor para proyecto de imágenes médicas

Este repositorio tiene una imagen de Docker que configura un contenedor
con las siguientes características:

- Disponibiliza un servicio de SSH que corre en el puerto 9022 del host (
i.e., calculin)  
    + El usuario y contraseña del servicio están en el archivo `passwd` en el
formato `usuario:contraseña`. Este archivo está en `.gitignore` para evitar
que se suba esta información a un repositorio público.
- Publica algunos puertos
    + El puerto 80 en el contenedor es el 9080 del host, el 443 es el 9443.
    + El rango de puertos 9100 a 9110 del contenedor se publica directamente en el
host.
- Establece un volumen en el contenedor en la ubicación `/web/`. Este directorio
es persistente y el código junto con los datos deberían estar allí.

