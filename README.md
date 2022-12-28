# docker-cache
Docker registry pull through cache setup with docker compose

## docker proxy
```
docker compose up -d
```

## docker client configuration
To configure docker to use this cache as a mirror, edit the daemon.json, and add:

/etc/docker/daemon.json

```
{
  "registry-mirrors" : ["http://192.168.0.80:5000"]
}
```

Then restart docker:
```
sudo service docker restart
```
