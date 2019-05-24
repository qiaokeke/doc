* https://github.com/cdr/code-server
## install with docker

```
docker run -it -d --user root -p 127.0.0.1:8443:8443 -v "${PWD}:/home/coder/project" codercom/code-server --allow-http --no-auth
```

## nginx配置
```
location / {
                        proxy_pass http://code-server.com/;
                        proxy_http_version 1.1;
                        proxy_set_header Upgrade $http_upgrade;
                        proxy_set_header Connection 'upgrade';
                        proxy_set_header Host $host;
                        proxy_cache_bypass $http_upgrade;
                        proxy_set_header X-Real-IP $remote_addr;
                        proxy_set_header Accept-Encoding gzip;
                        proxy_intercept_errors on;
                        error_page 404 502 /404.html;
                }

```
