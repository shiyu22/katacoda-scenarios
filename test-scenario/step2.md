#### 2. Download data and Run mols-search-webserver docker

```
$ wget https://raw.githubusercontent.com/milvus-io/bootcamp/1.0/solutions/mols_search/smiles-data/test_1w.smi
$ docker run -d -v <DATAPATH>:/tmp/data -p 35001:5000 -e "MILVUS_HOST=192.168.1.25" -e "MILVUS_PORT=19530" milvusbootcamp/mols-search-webserver:1.1.0
```

Refer to the following table for the parameter description:

| Parameter                     | Description                                                  |
| ----------------------------- | ------------------------------------------------------------ |
| -v DATAPATH:/tmp/data         | -v specifies directory mapping between the host and the docker image. Please modify `DATAPATH` to your local path of test_1w.smi. |
| -p 35001:5000                 | -p specifies pot mapping between the host and the image.     |
| -e "MILVUS_HOST=192.168.1.25" | -e specifies the system parameter mapping between the host and the image. Pease modify `192.168.1.25` to the IP address of the Milvus docker. |
| -e "MILVUS_PORT=19530"        | Pease modify `19530` to the port of Milvus docker.           |

#### 