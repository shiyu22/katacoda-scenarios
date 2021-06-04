#### 3. Run mols-search-webclient docker

```
$ docker run -d -p 8001:80 -e API_URL=http://192.168.1.25:35001 milvusbootcamp/mols-search-webclient:0.3.0
```

> Note: Please modify `192.168.1.25` to the IP address of the Milvus docker.