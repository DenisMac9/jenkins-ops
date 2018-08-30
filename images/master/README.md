Jenkins Docker Image
====================

Build de l'image
----------------

```
chmod +x build.sh
./build.sh
```

Lancement de l'image
--------------------

```
docker run -d -p 8080:8080 -p 50000:50000 \
    -e DOCKER_GROUP_ID=999 \
    -v jenkins_data_test:/var/jenkins_home \
    -v /var/run/docker.sock:/var/run/docker.sock \
    n1c0l4stournier/jenkins:lts-alpine
```
