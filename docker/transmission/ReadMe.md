For transmission to transfer the completed downloads onto a synology nfs share, first create an external volume

```docker
docker volume create --driver local --opt type=nfs --opt o=addr=bananas.home,rw --opt device=:/volume1/downloads bananas_downloads
```
and then run ```docker-compose up -d```


Upon start, transmission attempts to chown the /data/completed directory, so make sure that the uid and gid in your docker-compose.yml
```yaml
  environment:
    - PUID=1028
    - PGID=100
```
match the userid and groupid of your synology setup (e.g. 1028:100).

