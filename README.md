# Docker Jenkins
trying to setup Jenkins on linux server using docker


# Setup with `docker`:
```bash
docker run -u root -d --name myContainer -p 8080:8080 -v jenkins-data:/var/jenkins_home -v /var/run/docker.sock:/var/run/docker.sock -v "$HOME":/home jenkinsci/blueocean
```
or using `docker compose`:
```bash
docker compose -f docker-compose.yml up --build -d
```

Take it all down
```bash
docker compose -f docker-compose.yml down --remove-orphans --rmi local --volumes
```
