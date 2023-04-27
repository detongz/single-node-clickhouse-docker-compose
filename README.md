# Single Node Clickhouse docker compose

Use Docker compose, start single node clickhouse node, with no zookeeper, no network configs.

For testing purposes.

Your local folder `./data` is used for clickhouse's data storage.

*Supports Apple Silicon*

## Connect to clickhouse client

1. Docker compose start

```sh
docker-compose up -d
```

2. Connect to clickhouse with mysql client

```sh
mysql --protocol tcp -u default -P 9004 -ptest
```

## Default user and password

- name: default
- password: test