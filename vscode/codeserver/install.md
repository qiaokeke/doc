* https://github.com/cdr/code-server
## install with docker

```
docker run -it -p 127.0.0.1:8443:8443 -v "${PWD}:/home/coder/project" codercom/code-server --allow-http --no-auth
```
