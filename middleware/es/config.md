* v6.8


```
sysctl -w vm.max_map_count=262144

查看结果：

sysctl -a|grep vm.max_map_count

显示：

vm.max_map_count = 262144

 

上述方法修改之后，如果重启虚拟机将失效，所以：

解决办法：

在   /etc/sysctl.conf文件最后添加一行

vm.max_map_count=262144
```

```
# transport
transport.host: 10.170.0.12
# discovery
discovery.zen.ping.unicast.hosts: ["10.170.0.11", "10.170.0.12"]

#cluster
cluster.name: kk6-hkc-mid

#jvm.options
-Xms2g
-Xmx2g

```
