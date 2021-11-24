# docker-compose-prometheus-exporter-elasticsearch

Project to setup Prometheus Monitoring and Grafana to monitor Elasticsearch 

## List of components:

1. Prometheus
2. Grafana
4. Elasticsearch
6. Elasticsearch Prometheus Exporter

## What is the exporter

Learn more about exporters in Prometheus [here](https://prometheus.io/docs/instrumenting/exporters/). 


## Prometheus `config/promethues.yaml` file

Time series database

Read [here](https://prometheus.io/docs/prometheus/latest/configuration/configuration/) to know more about Prometheus Configuration.


## Pushgateway

Pushgateway is used to collect data from batch jobs or services:

To push data, simple execute:

```
echo "pipeline_job_metrics 3.141" | curl --data-binary @- http://user:pass@localhost:9091/metrics/job/pipeline_job
```

Replace `user:pass` with your user and password. Default `admin:admin`
