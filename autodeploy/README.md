# Docker容器

## 服务端:

```
docker build -f Dockerfile -t sss .
docker run -d --restart=always --name=sss -v {$path}/config.json:/ServerStatus/server/config.json -p {$port}:80 -p {$port}:35601 sss
```

## 客户端:

```
wget --no-check-certificate -qO client-linux.py 'https://raw.githubusercontent.com/cppla/ServerStatus/master/clients/client-linux.py' && nohup python client-linux.py SERVER={$SERVER} USER={$USER} PASSWORD={$PASSWORD} >/dev/null 2>&1 &
```

附: docker安装

```bash
curl -sSL https://get.docker.com/ | sh
```