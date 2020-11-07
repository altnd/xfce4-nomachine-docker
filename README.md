# XFCE4 Nomachine Docker
Ubuntu Desktop 18.04 (xfce) Dockerfile with NoMachine remote access and firefox, libreoffice & more

### Build

```
git clone https://github.com/capriciousduck/xfce4-nomachine-docker.git
cd xfce4-nomachine-docker
docker build -t=xfce4-nomachine-docker .
```


### Enviroment vaiables
* `USER` -> Username. Default is "admin"
* `PASSWORD` -> password for the nomachine login. Default is "password"

### Usage

```
docker run -d --rm -p 4000:4000 -p 4080:4080 -p 4443:4443 --name xfce4-desktop -e PASSWORD='your password' --cap-add=SYS_PTRACE xfce4-nomachine-docker
```



# Connect to the container
## with the Client
Download the NoMachine client from: https://www.nomachine.com/download, install the client, create a new connection to your public ip, port 4000, NX protocol, use user and password(from environmental variable) for authentication (make sure to setup password enviroment variable for that).

# xfce4-nomachine-container
