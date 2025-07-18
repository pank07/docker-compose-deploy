## Installation of buildpacks

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
