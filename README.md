### start
clear the cluster_conf exclude redis.conf if need
```
rm -f ./cluster_conf/64*/*
```

run redis_cluster_configs to generate cluster configurations
```
chmod +x ./redis_cluster_configs.sh
sh ./redis_cluster_configs.sh
```

after the container started, start redis cluster
```
docker exec -it redis_cluster /bin/bash ./bin/start_redis_cluster.sh
```
