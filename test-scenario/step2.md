#### 2. Download data and Run mols-search-webserver docker

`wget -P /root/data https://raw.githubusercontent.com/milvus-io/bootcamp/1.0/solutions/mols_search/smiles-data/test_1w.smi`{{execute}}
`docker run -d -v /root/data:/tmp/data -p 5000:5000 milvusbootcamp/mols-search-webserver:1.1.0`{{execute}}

Refer to the following table for the parameter description:

| Parameter                     | Description                                                  |
| ----------------------------- | ------------------------------------------------------------ |
| -v /root/data:/tmp/data         | -v specifies directory mapping between the host and the docker image.  |
| -p 5000:5000                 | -p specifies pot mapping between the host and the image.     |