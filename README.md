# Comandos-para-instalar-o-docker


#!/bin/sh
# instalar docker
sudo curl -fsSL http://get.docker.com | bash

# instalar docker-compose
sudo curl -L "https://github.com/docker/compose/releases/download/1.25.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose
docker-compose --version

# cria arquivo docker-compose.yml
# inicializar container
docker-compose up -d

# verificar containers
docker ps

# parar container
docker stop id_container

# remover containers parados
docker system prune -a -f --volumes
