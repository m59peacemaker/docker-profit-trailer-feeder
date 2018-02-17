# pmkr/profit-trailer-feeder

[![pmkr/profit-trailer-feeder on Docker Hub](https://img.shields.io/badge/Docker%20Hub-Hosted-blue.svg)](https://hub.docker.com/r/pmkr/profit-trailer-feeder/)

> [ProfitTrailer Feeder](https://github.com/mehtadone/PTFeeder) docker image.

Also check out [pmkr/profit-trailer](https://hub.docker.com/r/pmkr/profit-trailer).

## example

```sh
$ docker run -it \
-v $PWD/config/feeder:/appdata/config/feeder \
-v $PWD/config/
-v $PWD/config/pt:/config \
-v $PWD/logs/ptfeeder:/logs \
pmkr/profit-trailer-feeder
```

## volumes

### `/appdata/config/feeder`

Mount the Feeder config directory containing `hostsettings.json` and `appsettings.json` here.

### `/appdata/config/pt`

Mount the ProfitTrailer directory containing `application.properties` and `configuration.properties` here.

### `/appdata/logs`

Mount the directory for Feeder logs here.

## bin

### `startup`

This symlinks your config and logs into the appropriate Feeder directories and then starts Feeder.

### `feeder`

Just starts Feeder. You should usually use `startup` instead.
