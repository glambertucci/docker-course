# Ejercicio 6
## Lo primero es ir a este sitio
https://catalog.redhat.com/software/containers/redhat-openjdk-18/openjdk18-openshift/58ada5701fbe981673cd6b10
De ahi buscas la manera de registrarte con un usuario, te haces el usuario, aceptas terminos y condiciones que esta en otra pagina, y despues tiras un 
`docker pull registry.redhat.io/redhat-openjdk-18/openjdk18-openshift:1.15-1`
y es importante ponerlo bien en el dockerfile
## Despues haces la imagen igual que en el 4
`docker build -t ej6 . --build-arg JAR_FILE=./passwordapi.jar`

## Luego de corre la imagen creada
`docker run -d -p 8080:8080 ej6`
## Una vez que se verifica el funcionamiento yendo  a http://localhost:8080/. Se debe logear en dockerhub
`docker login`
## Yo en particular le tuve que cambiar el nombre, lo podria haber hecho bien desde el vamos
`docker tag ej6:latest glambertucci/ej6`
## Push
`docker push glambertucci/ej6:latest`

# Link a dockerhub
https://hub.docker.com/repository/docker/glambertucci/ej6
