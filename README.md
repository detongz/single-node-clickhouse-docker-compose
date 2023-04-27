# Single Node Clickhouse docker compose

Use Docker compose, start single node clickhouse node, with no zookeeper, no network configs.

For testing purposes.

Your local folder `./data` is used for clickhouse's data storage.

Configurations are `config.xml` and `user.xml`, refer to [doc](https://clickhouse.com/docs/en/operations/settings/settings-users).

*Supports Apple Silicon*

## Connect to clickhouse client

1. Download clickhouse into ./clickhouse:
```sh
curl -O 'https://builds.clickhouse.com/master/macos/clickhouse' && chmod a+x ./clickhouse
```

## Connect to clickhouse

```sh
./clickhouse client -h 127.0.0.1 --port 8123 -u user1 --password test --database test
```

You should see a smiling face as it connects to your service running on localhost:
```
my-host :)
```


## Default user and password

- name: user1
- password: test