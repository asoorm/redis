# Example 6-Node Redis Cluster Configuration

1. Provision 3 machines which are able to speak with each other (or run all locally)
2. Install Redis Server on each of them
3. Start 2 redis servers on each machine and ensure that you pass config file to each

```
./redis-server node1.conf
./redis-server node2.conf
./redis-server node3.conf
...
```
4. Create cluster by using redis-trib.rb ruby script

```
./redis-4.0.10/src/redis-trib.rb create --replicas 1 127.0.0.1:7001 127.0.0.1:7002 127.0.0.1:7003 127.0.0.1:7004 127.0.0.1:7005 127.0.0.1:7006
```

You will need to type `yes` to accept the cluster configuration

