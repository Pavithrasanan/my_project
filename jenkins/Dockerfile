FROM jenkins/jenkins
USER root
RUN apt-get update && apt-get install -y docker.io
USER jenkins
ARG DOCKER_GID=107
RUN groupadd -for -g ${DOCKER_GID} docker && \
    usermod -aG docker jenkins
