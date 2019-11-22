* https://randling.wordpress.com/2012/12/22/maven-over-socks-proxy/
```
mvn -U clean install -DsocksProxyHost='127.0.0.1' -DsocksProxyPort=8085
mvn -U clean install -DsocksProxyHost='op' -DsocksProxyPort=10808 '-Dmaven.test.skip=true'
```
