# **docker-compose-elasticsearch-kibana**

# **Overview**
Docker Compose for 3 Node Elasticsearch (7.2.0) Cluster and Kibana (7.2.0) Instance for development purposes.

- [x] 3 Node Elasticsearch version 7.2.0
- [x] Kibana version 7.2.0
- [x] Audit Beat version 7.2.0
- [x] Metric Beat version 7.2.0
- [x] Heart Beat version 7.2.0
- [x] Packet Beat version 7.2.0
- [x] File Beat version 7.2.0
- [x] APM Server version 7.2.0
- [x] APM Search 7.2.0
- [x] NGINX

# **NOTES**
- If you need Open Source version then change Elasticsearch and Kibana Images to elasticsearch-oss and kibana-oss respectively.
- Kibana is being served behind Nginx Proxy so you can secure access of kibana for your purpose.

# **COMING UP DOCKER APPLICATION PACKAGE FOR SWARM**

## **Requirements**
- [x] Docker 18.05
- [x] Docker-compose 1.21

### **Start Stack in Daemon Mode**
```
docker-compose up -d
```

### **Check status of docker-compose cluster**
```
docker-compose ps -a
```
![](images/dockerps.png)


### **Stop Compose Stack**
```
docker-compose down
```

### **Cluster Node Info**
```
curl http://localhost:9200/_nodes?pretty=true
```

### **Access Kibana**
```
http://localhost:5601
```

## **Validate Kibana is running**
![](images/kibana.png)

### **Access Elasticsearch**
```
http://localhost:9200
```
## **Validate Elasticsearch is running**
```json
{
  "name": "ff212cad143f",
  "cluster_name": "docker-cluster",
  "cluster_uuid": "0ecH5OZBS02odQeZSZip-Q",
  "version": {
    "number": "7.2.0",
    "build_flavor": "default",
    "build_type": "docker",
    "build_hash": "508c38a",
    "build_date": "2019-06-20T15:54:18.811730Z",
    "build_snapshot": false,
    "lucene_version": "8.0.0",
    "minimum_wire_compatibility_version": "6.8.0",
    "minimum_index_compatibility_version": "6.0.0-beta1"
  },
  "tagline": "You Know, for Search"
}
```

# **Resources**
* [Hands on Elasticsearch](https://medium.com/@maxy_ermayank/hands-on-elasticsearch-8fa59d8aebfc)
* [Elasticsearch Resources](https://medium.com/@maxy_ermayank/elasticsearch-resources-27d24f01c1dc)
* [Open Distro Elasticsearch](https://medium.com/@maxy_ermayank/tl-dr-aws-open-distro-elasticsearch-fc642f0e592a)
