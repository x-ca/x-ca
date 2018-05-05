# X-CA 

ref https://www.xiexianbin.cn/s/ca

## gen

```
git clone https://github.com/x-ca/x-ca.git
cd x-ca
docker run -it -d --privileged=true \
  -p 8080:80 \
  -p 8443:443 \
  -v ${pwd}:/root/x-ca:rw \
  --name x-ca ubuntu:16.04 bash
```
