Cluster Setup
1. Create the Kubernetes Cluster

Create a Kind cluster using the configuration file kind-config.yaml.

kind create cluster --config kind-config.yaml --name tws-kind-cluster

2. Docker Setup
Add the current user to the Docker group
sudo usermod -aG docker "$USER"

Apply the group changes
newgrp docker

Start the Docker service
sudo systemctl start docker

Enable Docker to start automatically on boot
sudo systemctl enable docker

Verify Docker Installation
docker --version
docker ps
