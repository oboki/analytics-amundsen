# analytics-amundsen

## requirements

### images

```bash
amundsendev/amundsen-frontend   3.1.0            cacf37b58d31   2 months ago    767MB
amundsendev/amundsen-search     2.4.1            d8902cbab16c   3 months ago    170MB
amundsendev/amundsen-metadata   3.0.0            2e4edc1d3f29   3 months ago    323MB
postgres                        9.6              bb00980cabc0   3 months ago    200MB
puckel/docker-airflow           1.10.9           3e408baf20fe   11 months ago   797MB
neo4j                           3.3.0            6919e3e3d3d5   21 months ago   192MB
elasticsearch                   6.7.0            02982be5777d   22 months ago   810MB
```

### kernel params

* docker-compose error: es_amundsen | [1]: max virtual memory areas vm.max_map_count [65530] is too low, increase to at least [262144]
* Increase the heap memory detailed instructions here
  * Edit `/etc/sysctl.conf`
  * Make entry `vm.max_map_count=262144`. Save and exit.
  * Reload settings `$ sysctl -p`
  * Restart `docker-compose`