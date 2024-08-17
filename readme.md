# Home Assistant

https://github.com/BenJ1337/docker_ha_home-assistant-bootstrap


```
mkdir ~/certs/
openssl req -x509 -newkey rsa:4096 -keyout ~/certs/ca-private.pem -out ~/certs/ca-root.crt -sha256 -days 3650 -addext keyUsage=keyCertSign -nodes -subj "/C=AT/ST=/L=/O=/OU=/CN=BenjaminHackerCA"

openssl req -new -nodes -out ~/certs/ha.csr -newkey rsa:4096 -keyout ~/certs/ha-private.pem -subj "/C=AT/ST=/L=/O=/CN=172.16.0.90"
openssl x509 -req -in ~/certs/ha.csr -CA ~/certs/ca-root.crt -CAkey ~/certs/ca-private.pem -CAcreateserial -out ~/certs/ha.crt -days 3650 -sha256
```
