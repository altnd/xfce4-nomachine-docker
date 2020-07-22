# Docker VDI (Virtual Desktop Instance)
Ubuntu Desktop 18.04 (xfce) Dockerfile with NoMachine remote access and firefox, chromium & more

### Build

```
git clone <URL>
cd docker-vdi
docker build -t=docker-vdi .
```


### Enviroment vaiables
* `PASSWORD` -> password for the nomachine login

### Usage

```
docker run -d --rm -p 4000:4000 -p 4080:4080 -p 4443:4443 --name docker-vdi -e PASSWORD=password --cap-add=SYS_PTRACE capriciousduck/docker-vdi
```



# Connect to the container
## with the Client
Download the NoMachine client from: https://www.nomachine.com/download, install the client, create a new connection to your public ip, port 4000, NX protocol, use user 'admin' and password(from environmental variable) for authentication (make sure to setup password enviroment variable for that).

## via Webbrowser (only with Enterprise Client)
open URL: `https://127.0.0.1:4443`
# xfce4-nomachine-container
