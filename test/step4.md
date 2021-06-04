#### 4. Launch a browser

```
# Please modify IP address and port according the previous configurations
http://192.168.1.25:8001
```

## How to use

- Initial interface

[![img](https://github.com/milvus-io/bootcamp/raw/master/solutions/molecular_similarity_search/quick_deploy/pic/init_status.PNG)](https://github.com/milvus-io/bootcamp/blob/master/solutions/molecular_similarity_search/quick_deploy/pic/init_status.PNG)

- Load chemical structures
  1. In `path/to/your/data`, enter the location of the smi file. For example, `/tmp/data/test_1w.smi`.
  2. Click `+` to load.
  3. You can see the number of chemical structures have changed: 10000 Molecular Formula in this set

[![img](https://github.com/milvus-io/bootcamp/raw/master/solutions/molecular_similarity_search/quick_deploy/pic/load_data.PNG)](https://github.com/milvus-io/bootcamp/blob/master/solutions/molecular_similarity_search/quick_deploy/pic/load_data.PNG)

- Search chemical structures
  1. Enter the chemical structure to search, such as `Cc1ccc(cc1)S(=O)(=O)N`, and press <ENTER>.
  2. Set the value of topk. This demo returns topk most similar chemical structures.

[![img](https://github.com/milvus-io/bootcamp/raw/master/solutions/molecular_similarity_search/quick_deploy/pic/search_data.PNG)](https://github.com/milvus-io/bootcamp/blob/master/solutions/molecular_similarity_search/quick_deploy/pic/search_data.PNG)

- Clear chemical structure data

  Click `CLEAR ALL` to remove all chemical structure data.

[![img](https://github.com/milvus-io/bootcamp/raw/master/solutions/molecular_similarity_search/quick_deploy/pic/delete_data.PNG)](https://github.com/milvus-io/bootcamp/blob/master/solutions/molecular_similarity_search/quick_deploy/pic/delete_data.PNG)