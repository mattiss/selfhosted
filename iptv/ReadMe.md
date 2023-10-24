Create a local volume to store playlists

```docker
docker volume create --driver local \
  --opt type=none \
  --opt device=/home/mattiss/docker/iptv/playlists \
  --opt o=bind \
  iptv_playlists
```