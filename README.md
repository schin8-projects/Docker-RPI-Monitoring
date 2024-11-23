# Docker-RPI-Monitoring

Based on Oijkn's [Docker-RAspberry-PI-Monitoring](https://github.com/oijkn/Docker-Raspberry-PI-Monitoring/tree/main?tab=MIT-1-ov-file) repository.

This version exposes the Prometheus service port to allow monitoring of other hosts.

# Setup

Create grafana user

```
 sudo groupadd -g 472 grafana
 sudo useradd grafana -u 472 -g 472 -r
  
```

As the pi user

```
cd ~
mkdir installs
cd $_
git clone https://github.com/schin8-projects/Docker-RPI-Monitoring.git
cd Docker-RPI-Monitoring
```



```
mkdir -p prometheus/data grafana/data && \
sudo chown -R 472:472 grafana/ && \
sudo chown -R 65534:65534 prometheus/
```

Startup Stack
Portainer installed docker uses "docker compose", otherwise try "docker-compose"

```
# Install all monitoring components
docker compose up -d

# Install only the collectors
docker compose -f docker-compose.collectors.yaml up -d

```

