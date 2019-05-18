### install jenkins with docker
```
# pull
docker pull jenkins

```
### run
```
docker run   -u root   --rm   -d   -p 8080:8080   -p 50000:50000   -v jenkins-data:/var/jenkins_home   -v /var/run/docker.sock:/var/run/docker.sock   jenkinsci/blueocean
```
### passwd
docker exec -it jenkins bash
###

### nginx
```
server{
        server_name jenkins.kk1-twb-middle1.qiaokeke.top;
        location / {
                proxy_pass http://127.0.0.1:8080/;
        }
}
```
