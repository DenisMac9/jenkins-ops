FROM openjdk:8

COPY swarm-client-3.13.jar swarm-client.jar

COPY entrypoint.sh entrypoint.sh
RUN chmod +x entrypoint.sh

RUN curl https://get.docker.com/builds/Linux/x86_64/docker-latest.tgz | tar xvz -C /tmp/ && mv /tmp/docker/docker /usr/bin/docker

ENTRYPOINT ["./entrypoint.sh"]
