# Ejercicio 4
## Aqui se crea la imagen, donde dice app.jar va el nombre.
`docker build -t app.jar . --build-arg JAR_FILE=./passwordapi.jar`
## Luego de corre la imagen creada
`docker run -d -p 8080:8080 app.jar`
## Una vez que funciona se debe logear en dockerhub
`docker login`
## Yo en particular le tuve que cambiar el nombre, lo podria haber hecho bien desde el vamos
`docker tag app.jar:latest glambertucci/app.jar`
## Push
`docker push glambertucci/app.jar:latest`

# Link a dockerhub
https://hub.docker.com/repository/docker/glambertucci/app.jar