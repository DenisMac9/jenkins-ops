Jenkins Swarm client Docker image
=================================

TODO
----

- Passer le client en mode authentifié
- Ajouter l'URL du master Jenkins en variable d'environnement

Build de l'image
----------------

```
chmod +x build.sh
./build.sh
```

Lancement de l'image
--------------------

```
docker run -d \
    -v /var/run/docker.sock:/var/run/docker.sock \
    n1c0l4stournier/swarm-client:3.13.0
```
