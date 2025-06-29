# Day-02: Docker + Docker Compose

## Goal: Master containerization and local orchestration

✅ Dockerfile writing: multi-stage, optimized builds

✅ Docker networking, volumes, exec/debug containers

✅ Docker Compose: multi-container setups (e.g., Node.js + MongoDB)

✅ Docker Hub pushes/pulls

Hands-on:

- Containerize a full-stack app

- Use Docker Compose to run the app

- Debug container failures


### Add your user to the Docker group to enable running Docker without using sudo
sudo usermod -aG docker $USER
### Log out and log back in to apply the group changes.
### Alternatively, run the following command to activate the new group membership without logging out.
newgrp docker
