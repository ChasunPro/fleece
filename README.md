# fleece

青龙官方搭建脚本
```
# curl -sSL get.docker.com | sh
docker run -dit \
  -v $PWD/ql/data:/ql/data \
  # 冒号后面的 5700 为默认端口，如果设置了 QlPort, 需要跟 QlPort 保持一致
  -p 5700:5700 \
  # 部署路径非必须，比如 /test
  -e QlBaseUrl="/" \
  # 部署端口非必须，当使用 host 模式时，可以设置服务启动后的端口，默认 5700
  -e QlPort="5700" \
  --name qinglong \
  --hostname qinglong \
  --restart unless-stopped \
  whyour/qinglong:latest
```
青龙搭建python3.10
```
docker run -dit \
  -v $PWD/ql:/ql/data \
  -p 5700:5700 \
  --name ql-debian \
  --hostname ql-debian \
  --restart unless-stopped \
  whyour/qinglong:debian-python3.10
```
青龙搭建qinglong:2.17.9
```
docker run -dit \
  -v $PWD/ql:/ql/data \
  -p 5700:5700 \
  --name qinglong \
  --hostname qinglong \
  --restart unless-stopped \
  whyour/qinglong:2.17.9
```
