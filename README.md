# This is a simple notes app built with React and Django.

## Requirements
1. Python 3.9
2. Node.js
3. React

## Installation
1. Clone the repository
```
git clone https://github.com/pank07/docker-compose-django-notes-app.git
```

2. Build the app
```
docker build -t notes-app .
```

3. Run the app
```
docker run -d -p 8000:8000 notes-app:latest
```

## Nginx

Install Nginx reverse proxy to make this application available

`sudo apt-get update`
`sudo apt install nginx`

# Installation of cloud native buildpacks (run without dockerfile)

#steps
- Update your machine
```bash
sudo apt update
```

- Install docker
``bash
sudo apt install docker.io -y
```

- permission to ubuntu user to docker group
```bash
sudo usermod -aG docker $USER && newgrp docker
```

- Install pack utility to build image
```bash
sudo add-apt-repository ppa:cncf-buildpacks/pack-cli
sudo apt-get update
sudo apt-get install pack-cli
```

- code clone
```bash
git clone <git_repo>
 ```

- command to get pack builder
```bash
pack build suggest
```

- Copy the google builder and paste in the command
```bash
pack build --builder=<choose-builder-from-above-command> my-app-image
```

- After build, check images
```bash
docker images
```

- Run the images as a container
```bash
docker run -d -p <8080:8080> my-app-image:tag
```

- Access application
```bash
http://<PUBLIC-IP>:8000
```

