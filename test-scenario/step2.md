#### 2. Download data and Run mols-search-webserver docker

Download the smiles data with molecular.
`wget -P /root/data https://raw.githubusercontent.com/milvus-io/bootcamp/1.0/solutions/mols_search/smiles-data/test_1w.smi`{{execute}}

Run server with Docker.
`docker run -d -v /root/data:/tmp/data -p 5000:5000 --network my-net --ip 10.0.0.3 -e "MILVUS_HOST=10.0.0.2" milvusbootcamp/mols-search-webserver:1.1.0`{{execute}}

Refer to the following table for the parameter description:

| Parameter                     | Description                                                  |
| ----------------------------- | ------------------------------------------------------------ |
| -v /root/data:/tmp/data         | -v specifies directory mapping between the host and the docker image.  |
| -p 5000:5000                 | -p specifies pot mapping between the host and the image.     |
