As describeD in https://www.smarthomebeginner.com/traefik-docker-nextcloud/

```shell
setfacl -d -m g::r -m o::--- ~/docker
sudo mkdir ~/docker/secrets
sudo setfacl -d -m g::--- ~/docker/secrets

docker exec -it nextcloud bash
apt update
apt install nano
nano config/config.php
  'overwriteprotocol' => 'https',

```