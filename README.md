# elk
Project developed during ELK training course from UDEMY

1. Installation:

https://www.digitalocean.com/community/tutorials/how-to-install-elasticsearch-logstash-and-kibana-elastic-stack-on-ubuntu-20-04-pt

https://logz.io/blog/deploying-the-elk-stack-on-kubernetes-with-helm/

https://www.magalix.com/blog/kubernetes-observability-log-aggregation-using-elk-stack

https://citizix.com/how-to-install-and-configure-elasticsearch-on-opensuse-leap-15-3/

PS: f necessary disable machine learn module by adding "xpack.ml.enabled: false" on /etc/elasticsearch/elasticsearch.yml

2. Installing and indexing the shakespeare work:

Download mapp file:
```
wget http://media.sundog-soft.com/es7/shakes-mapping.json
```

Create index:
```
curl -H 'Content-Type: application/json' -XPUT 127.0.0.1:9200/shakespeare --data-binary @shakes-mapping.json
```

Download data:
```
wget http://media.sundog-soft.com/es7/shakespeare_7.0.json
```

Insert data into el:
```
curl -H 'Content-Type: application/json' -XPOST '127.0.0.1:9200/shakespeare/_bulk?pretty' --data-binary @shakespeare_7.0.json
```

Search for a a text content:
```
curl -H 'Content-Type: application/json' -XGET '127.0.0.1:9200/shakespeare/_search?pretty' -d '
```

Then

    {
    "query" : {
    "match_phrase" : {
    "text_entry" : "to be or not to be"
    }
    }
    }
    '

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
https://citizix.com/how-to-install-and-configure-elasticsearch-on-opensuse-leap-15-3/
