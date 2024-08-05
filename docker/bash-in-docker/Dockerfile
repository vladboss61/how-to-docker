FROM ubuntu
MAINTAINER The Ubuntu/ vlad_delas 

# Volumes for systemd
# VOLUME ["/run", "/tmp"]

# Environment for systemd
# ENV container=docker

RUN addgroup --group dotnet --gid 2000 && `
    adduser --disabled-password --uid 1000 --gid 2000 "dotnet" --gecos '' && `
    chown -R dotnet:dotnet /app

USER dotnet:dotnet

# For systemd usage this changes to /usr/sbin/init
# Keeping it as /bin/bash for compatability with previous
# to build image : docker build . -t ubuntu_bash
# to start: docker run -t --name container_name -d ubuntu-bash
# to attach docker exec -it `container_name or id of container` /bin/bash
CMD ["/bin/bash"]
