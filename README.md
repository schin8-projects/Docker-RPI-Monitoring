# Docker-RPI-Monitoring

Based on Oijkn's [Docker-RAspberry-PI-Monitoring](https://github.com/oijkn/Docker-Raspberry-PI-Monitoring/tree/main?tab=MIT-1-ov-file) repository.

This version exposes the Prometheus service port to allow monitoring of other hosts.

# Setup

Clone this repository, in this case we'll clone to the "/home/pi/installs" directory.

Next make sure to update the user and groups

```
mkdir -p prometheus/data grafana/data && \
sudo chown -R 472:472 grafana/ && \
sudo chown -R 65534:65534 prometheus/
```

