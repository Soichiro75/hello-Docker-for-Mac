# hello-docker-for-mac

## Install Docker for Mac

**This procedure is Docker for Mac installation, NOT Docker Toolbox**

- Go to [Docker Page](https://www.docker.com/products/docker).

  - Note:
    - "Docker for Mac" is currently in public beta.
    - System Requirements: Docker for Mac will launch only if all these requirements are met.
      - Mac must be a 2010 or newer model, with Intel’s hardware support for memory management unit (MMU) virtualization; i.e., Extended Page Tables (EPT)
      - OS X 10.10.3 Yosemite or newer
      - At least 4GB of RAM
      - VirtualBox prior to version 4.3.30 must NOT be installed (it is incompatible with Docker for Mac)

- Click `Download Docker for Mac` and `Save`

<img src="https://github.com/Soichiro75/hello-docker-for-mac/blob/master/images/2016-07-07_DownloadDockerDmg.png" width="320px">

- Double-click Docker.dmg to open the installer, then drag Moby the whale to the Applications folder.

<img src="https://github.com/Soichiro75/hello-docker-for-mac/blob/master/images/2016-07-11_01_InstallDocker.png" width="320px">

- Double-click Docker.app in your applications directory to start Docker.

<img src="https://github.com/Soichiro75/hello-docker-for-mac/blob/master/images/2016-07-11_02_OpenDocker.png" width="320px">

- A whale(<img src="https://github.com/Soichiro75/hello-docker-for-mac/blob/master/images/2016-07-11_06_whale-x.png">) in the top status bar indicates that Docker is running, and accessible from a terminal. Click the whale (<img src="https://github.com/Soichiro75/hello-docker-for-mac/blob/master/images/2016-07-11_06_whale-x.png">) in the status bar to dismiss this popup.

<img src="https://github.com/Soichiro75/hello-docker-for-mac/blob/master/images/2016-07-11_07_RunningDocker.png" width="320px">

- Click the whale (<img src="https://github.com/Soichiro75/hello-docker-for-mac/blob/master/images/2016-07-11_06_whale-x.png">) to get Preferences, and other options.

<img src="https://github.com/Soichiro75/hello-docker-for-mac/blob/master/images/2016-07-11_08_ClickTheWhale.png" width="320px">

- Check version of Docker Engine, Compose, and Machine

```
$ docker --version
Docker version 1.12.0-rc3, build 91e29e8, experimental

$ docker-compose --version
docker-compose version 1.8.0-rc1, build 9bf6bc6

$ docker-machine --version
docker-machine version 0.8.0-rc1, build fffa6c9
```


## Run Example App

- docker run -d -p 80:80 --name webserver nginx

- docker ps

```
CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS              PORTS                         NAMES
319bd7d2893f        nginx               "nginx -g 'daemon off"   43 seconds ago      Up 43 seconds       0.0.0.0:80->80/tcp, 443/tcp   webserver
```

- In a web browser, go to http://localhost/ to bring up the home page.

<img src="https://github.com/Soichiro75/hello-docker-for-mac/blob/master/images/2016-07-11_09_WelcomeToNginx.png" width="320px">

For more details, see [Getting Started with Docker for Mac](https://docs.docker.com/docker-for-mac/).
