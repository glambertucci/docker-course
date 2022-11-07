docker pull nicopaez/pingapp
docker login
docker tag nicopaez/pingapp:latest glambertucci/dockercourse
docker push glambertucci/dockercourse:latest

docker pull glambertucci/dockercourse:latest