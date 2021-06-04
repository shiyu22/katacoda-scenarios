#### 1. Run Milvus Docker

This demo uses Milvus 1.1.0 CPU version. Refer to [milvus.io](https://milvus.io/docs/v1.1.0/milvus_docker-cpu.md) to learn how to install and run Milvus.

First need to download the configuration file.

`wget -P /home/$USER/milvus/conf https://raw.githubusercontent.com/milvus-io/milvus/v1.1.0/core/conf/demo/server_config.yaml`{{execute}}

Then set Milvus server configuration, set `cache_size` to `512MB` and `insert_buffer_size` to `512MB` since the limitiom of memory.
`sed -i 's/cache_size: 4GB/cache_size: 512MB/g' /home/$USER/milvus/conf/server_config.yaml`{{execute}}

`sed -i 's/insert_buffer_size: 1GB/insert_buffer_size: 512MB/g' /home/$USER/milvus/conf/server_config.yaml`{{execute}}


Create a Docker network.
`docker network create my-net --subnet 10.0.0.0/16`{{execute}}


Run Milvus with Docker.
`docker run -d --name milvus_cpu_1.1.0 --network my-net --ip 10.0.0.2 -p 19530:19530 -p 19121:19121 -v /home/$USER/milvus/db:/var/lib/milvus/db -v /home/$USER/milvus/conf:/var/lib/milvus/conf -v /home/$USER/milvus/logs:/var/lib/milvus/logs -v /home/$USER/milvus/wal:/var/lib/milvus/wal milvusdb/milvus:1.1.0-cpu-d050721-5e559c`{{execute}}

Show the status.
`docker logs milvus_cpu_1.1.0`{{execute}}
