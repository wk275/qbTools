# qbTools

This repository installs tools for the QBUS environment

It creates docker compose files for
- node-red (handles Qbus logic)
- home-assistant (Qbus dashboard)
- mosquitto (mqtt message broker)
- influxDB (database for Qbus statistics)
- grafana (Qbus graphics)

Creates homeassistant entities for qbus via node-red subflows

## Prerequisites
- install qbusmqtt gateway
``` 
https://github.com/QbusKoen/QbusMqtt-installer
```
- install docker & docker compose
```
https://docs.docker.com/engine/install/
```
### Create docker container node-red-qbus
`ssh <your user>@<your server address>`

```
mkdir -p ~/docker/node-red-qbus
cd ~/docker/node-red-qbus
git clone https://github.com/wk275/qbus---nodered---homeassistant/node-red
docker compose up -d
docker ps -a
```
### login node-red
`http://<your server address>:1880`

