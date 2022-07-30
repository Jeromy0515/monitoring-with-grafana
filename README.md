# Monitoring with Grafana

### Architecture
![image](https://user-images.githubusercontent.com/77256585/181743469-41d9fd4b-cf6f-44fd-b68d-0fafd32173b5.png)

## Configure Docker
```
mv daemon.json /etc/docker/daemon.json
```
**OR**
```
sudo tee /etc/docker/daemon.json<<EOF
{
  "metrics-addr" : "0.0.0.0:9323",
  "experimental" : true
}
EOF
```

## How to deploy
```
docker stack deploy -c docker-compose.yml <stack-name>
```