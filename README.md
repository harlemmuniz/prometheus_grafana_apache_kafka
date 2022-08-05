# prometheus_grafana_apache_kafka
A monitoring project using Prometheus and Grafana for Apache Kafka

After clone the project and configure the Kafka to use the jmx-exporter, change the target broker ips in the prometheus.yml.

```
sudo docker run -p 9090:9090 -d --name=prometheus --restart unless-stopped -v /opt/prometheus:/etc/prometheus prom/prometheus

sudo docker run -p 3000:3000 -d --name=grafana --restart unless-stopped -e GF_AUTH_ANONYMOUS_ENABLED=true -e GF_AUTH_ANONYMOUS_ORG_ROLE=Admin -v grafana-storage:/var/lib/grafana grafana/grafana
```
