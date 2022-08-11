# Monitoring with Grafana

### Architecture
![image](https://user-images.githubusercontent.com/77256585/184115803-2242e2f0-18fa-433b-a1cb-4fe4129242f6.png)


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
docker stack deploy -c docker-stack.yml <stack-name>
```