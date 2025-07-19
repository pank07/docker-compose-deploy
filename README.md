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

# After written Docker-Compose file finally project deployed
<img width="1366" height="768" alt="Screenshot (52)" src="https://github.com/user-attachments/assets/7fb291c3-8022-483e-bcbd-74f32f950b4b" />
<img width="1366" height="768" alt="Screenshot (53)" src="https://github.com/user-attachments/assets/35528660-e8e1-43fa-9247-1d02a693b628" />
<img width="1366" height="768" alt="Screenshot (54)" src="https://github.com/user-attachments/assets/070e0f6e-9ac2-4c23-a579-06a824900a35" />


