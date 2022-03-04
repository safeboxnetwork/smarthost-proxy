The msarthost-proxy json files contain teh required information to deploy one loadbalancer (from haproxy) and minimum two backend proxies (from nginx) with terminating HTTPS process and translate it to HTTP to backend www and other services.

The loadbalancer process depend on dns service which is defined is json.

## How to run

```sh

# docker run \
 --detach \
 --rm \
 --volume /etc/user/config/services/:/services/:ro \
 --volume /var/run/docker.sock:/var/run/docker.sock \
 --volume /usr/bin/docker:/usr/bin/docker:ro \
 --volume /etc/user/config/services/tmp:/services/tmp:rw \
 registry.format.hu/setup:latest public-proxy.json start

```

## Templates in JSON format
