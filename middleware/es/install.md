* https://www.elastic.co/guide/en/elasticsearch/reference/current/targz.html
* https://www.elastic.co/guide/en/elasticsearch/reference/6.8/zip-targz.html
```
wget https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-7.3.1-darwin-x86_64.tar.gz
tar -xzf elasticsearch-7.3.1-darwin-x86_64.tar.gz
cd elasticsearch-7.3.1/ 

./bin/elasticsearch
./bin/elasticsearch -d -p pid

pkill -F pid
```
