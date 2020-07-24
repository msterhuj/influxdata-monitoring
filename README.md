# InfluxData monitoring

## Content
This docker compose file contains three services with influxdb v2 for stroring data, kapacitor for the alert system and chronograf for the management panel which communicates in the way described below.
| ![uml](https://www.influxdata.com/wp-content/uploads/InfluxData-Kapasitor.png) |
|--|
* Telegraf is not included but can be added manually

## Install & Start
Run this command on console
```
$ git clone https://github.com/msterhuj/influxdata-monitoring.git
$ cd influxdata-monitoring
$ docker-compose up -d
```
> -d is for start docker compose on deamon mode

For show log if docker app is on deamon run in same directory 
```
docker-compose logs -f
```
Quit logs press 'Ctrl + C'

> All data are saved on ./data in the same folder than docker-compose.yml

## Ports info
|    App     |    Service   | Port |
|------------|--------------|------|
|  influxdb  |   http api   | 8086 |
|  influxdb  |   udp api    | 8089 |
| chronograf | admin pannel | 8888 |

