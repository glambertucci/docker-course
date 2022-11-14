# HEALTHCHECK
### La instrucción HEALTHCHECK le dice a Docker cómo probar un contenedor para definir si continua funcionando. Esto puede detectar casos como un servidor web que está atascado en un bucle infinito y no puede manejar nuevas conexiones, aunque el proceso del servidor todavía se esté ejecutando.

### Cuando un contenedor tiene el HEALTHCHECK, tiene un estado HEALTHCHECK además de su estado normal. Comienza en un estado incial y cada vez que pasa una verificación de estado, se vuelve saludable (cualquiera que sea el estado en el que se encontraba anteriormente). Después de un cierto número de fallas consecutivas, se vuelve inestable.

Link a documentación: `https://docs.docker.com/engine/reference/builder/#:~:text=HEALTHCHECK%F0%9F%94%97,the%20new%20status.`

# ONBUILD 

### La instrucción ONBUILD agrega a la imagen una instrucción de trigger que se ejecutará en un momento posterior, cuando la imagen se use como base para otra construcción. El trigger se ejecutará en el contexto de la compilación 

### Cualquier instrucción de compilación se puede registrar como trigger.
### Esto es útil si está creando una imagen que se usará como base para crear otras imágenes, por ejemplo, un entorno de creación de aplicaciones o un daemon que puede personalizarse con una configuración específica del usuario.

Link a documentación: `https://docs.docker.com/engine/reference/builder/#onbuild:~:text=change%20between%20builds.-,ONBUILD,For%20example%20you%20might%20add%20something%20like%20this%3A,-ONBUILD%20ADD%20.%20/app`
# VOLUME
### La instrucción VOLUME crea un punto de montaje con el nombre especificado y lo marca como que contiene volúmenes montados externamente desde un host nativo u otros contenedores. El valor puede ser una matriz JSON, VOLUMEN ["/var/log/"] o una cadena sin formato con varios argumentos, como VOLUME /var/log o VOLUME /var/log /var/db.

Link a documentación: `https://docs.docker.com/engine/reference/builder/#volume:~:text=have%20a%20value.-,VOLUME,must%20specify%20the%20mountpoint%20when%20you%20create%20or%20run%20the%20container.,-USER`