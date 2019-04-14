### adding user to the docker group
```
sudo groupadd docker
sudo gpasswd -a $USER docker

newgrp docker

