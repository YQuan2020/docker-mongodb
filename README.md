#本地mongodb 副本集。

可以做各种关于副本集的实验。


启动
```` 
docker-compose up -d --build
````

进入container查看状态
````
docker exec -it mongo1 mongo
````

查看集群状态
````
rs.status()
````

如果集群状态异常，可以重新单独跑下creator的命令即可

secondary可以查询
````
rs.slaveOk() 
````

#reference
https://blog.yowko.com/docker-mongodb-replica-set/