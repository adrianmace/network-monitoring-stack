# network-monitoring-stack

## Installation

1. Determine the private IP of the host you're running this on (e.g. `192.168.1.123`)
2. Execute the following, substituing your own IP in the command
```
sed -i "s/{{HOST_IP}}/192.168.1.123/g" ./volumes/prometheus/prometheus.yml
```
3. Execute `docker-compose up -d`
4. Launch Grafana and create a prometheus datasource pointing to your host IP, then import the `dashboard.json` file.
