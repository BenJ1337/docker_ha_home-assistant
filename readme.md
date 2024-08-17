# Home Assistant

https://github.com/BenJ1337/docker_ha_home-assistant-bootstrap

## Setup

### Clone everything

```
git clone --recurse-submodules
```

or

```
$ git submodule init
$ git submodule update
```

### HA Secrets
```
$ cp config/secrets.yaml.template config/secrets.yaml
```

Configuration MariaDb and InfluxDb
```
$ nano config/secrets.yaml
```
