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
<img width="1366" height="485" alt="Screenshot (152)" src="https://github.com/user-attachments/assets/44777367-a674-4537-9ab6-70375ae8db40" />
- Copy the google builder and paste in the command

```bash
pack build --builder=<choose-builder-from-above-command> my-app-image
```

<img width="1366" height="768" alt="Screenshot (89)" src="https://github.com/user-attachments/assets/4529ac02-ed6f-4586-a6b3-f1a063b8f952" />
<img width="1366" height="768" alt="Screenshot (90)" src="https://github.com/user-attachments/assets/414b2cc7-0a60-4a22-a169-f52ef7ec0554" />
<img width="1366" height="768" alt="Screenshot (91)" src="https://github.com/user-attachments/assets/c7e70b0b-c26f-48c0-987f-4b945b37c79c" />
<img width="1366" height="768" alt="Screenshot (92)" src="https://github.com/user-attachments/assets/939272dc-eb42-4ff1-b20d-d538781c76d7" />

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

# After written Docker-Compose file finally project deployed
<img width="1366" height="768" alt="Screenshot (52)" src="https://github.com/user-attachments/assets/7fb291c3-8022-483e-bcbd-74f32f950b4b" />
<img width="1366" height="768" alt="Screenshot (53)" src="https://github.com/user-attachments/assets/35528660-e8e1-43fa-9247-1d02a693b628" />
<img width="1366" height="768" alt="Screenshot (54)" src="https://github.com/user-attachments/assets/070e0f6e-9ac2-4c23-a579-06a824900a35" />


