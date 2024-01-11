# Set up clickhouse server


## Setup Cluster

```
docker network create clickhouse-net
docker-compose up -d
```


```
docker run -it --rm --network="clickhouse-net" --link clickhouse1:clickhouse-server clickhouse/clickhouse-client --host clickhouse-server
```

```sql
SELECT *
FROM system.clusters 
```


