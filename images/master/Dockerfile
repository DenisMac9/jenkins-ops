FROM jenkins/jenkins:lts-alpine

USER root

ARG DEFAULT_DOCKER_GROUP_ID=999

ENV DOCKER_GROUP_ID=${DEFAULT_DOCKER_GROUP_ID}

RUN apk --no-cache add shadow && usermod -aG ${DOCKER_GROUP_ID} jenkins

RUN curl https://get.docker.com/builds/Linux/x86_64/docker-latest.tgz | tar xvz -C /tmp/ && mv /tmp/docker/docker /usr/bin/docker

USER jenkins