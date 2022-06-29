# elk
Project developed during ELK training course from UDEMY

1. Installation:

Ubuntu Installation

```
wget -qO - https://artifacts.elastic.com/GPG-KEY-elasticsearch | sudo apt-key add -
sudo apt-get install apt-transport-https
echo "deb https://artifacts.elastic.co/packages/7.x/apt stable main" | sudo tee -a /etc/apt/source.list.d/elastic-7.x.list
sudo apt-get update && sudo apt-get install elasticsearch
```


Persistent run into K8S (minikube)
Start an VM with 2gb RAM ,2vcpu and 20gb HD them
```
https://minikube.sigs.k8s.io/docs/start/
```

Setup configuration file

```
sudo nano /etc/elasticsearch/elasticsearch.yml
```

Uncomment the line `node.name: node-1`
Uncomment the line and edit: `network.host: 0.0.0.0`
Uncomment and edit: `discovery.seed_hosts: ["127.0.0.1"]`
Uncoment and edit: `cluster.initial_master_nodes: ["node-1"]`
Save and exit.


## Introduction
This step involves envronment configuration, Rest API and inverted index

## Mapping and Index
Mapp, index, import, export and delete data

## Searchs and Queris
Searchs, queries, filters, ordering, pagination, fuzzynes and partial match

## Import data
Scripts, libs, and csv/json importation using logstash

## Agregations
Aggregations and histograns

## Kibana
Index pattern, discover, graph, dash and dev tools]]

## Log analyses
Filebeat, xpack and filebeat

## Elastic on cloud
Amazon ES and elastic cloud
