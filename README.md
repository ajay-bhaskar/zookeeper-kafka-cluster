# Deploy 3 node Zookeeper and Kafka cluster on Kubernetes Cluster
### Versions:
* Zookeeper v3.6.2
* Zookeeper v2.6
* Kafka v2.11
### It uses host path as volumes for storage
### Steps to deploy:
1. On three different nodes run the following command:
    ```sh
    mkdir /tmp/zoo && chmod -R 777 /tmp/zoo
    mkdir /tmp/kafka && chmod -R 777 /tmp/kafka
    ```
2. Deploy Zookeeper Cluster:
    * To deploy Zookeeper v3.6.2
    ```sh
    kubectl apply -f Zookeeper/zookeeper_3.6.2.yaml
    ```
    * To deploy Zookeeper v2.6
    ```sh
    kubectl apply -f Zookeeper/zookeeper_2.6.yaml
    ```
3. Wait till Zookeeper cluster is up & running  
4. Deploy Kafka Cluster:
```sh
kubectl apply -f Kafka/kafka_2.11.yaml
```