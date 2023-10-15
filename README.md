# TOR in a Container
[![Docker
Pulls](https://img.shields.io/docker/pulls/threatcode/tor.svg?style=plastic)](https://hub.docker.com/r/threatcode/tor/)
![License](https://img.shields.io/badge/License-GPL-blue.svg?style=plastic)

TOR (The Onion Router) in a container. Easy, simple and fast way to publish
custom hidden services in the deepweb.

# Variables

- `PRIVATE_KEY` - Private key to be used by the hidden service.
- `LISTEN_PORT` - Port that the hidden service will listen to
- `REDIRECT` - To where the Tor will redirect the traffic (your server), in the
  format `host:port`.
- `PROXY_PORT` - If you want to enable Tor Proxy Socks, use this variable to set
  which port you want tor listening to.

# Generating a private key

To generate your private key run the following command:

```
docker run -it --rm --entrypoint shallot threatcode/tor-hiddenservice-nginx <pattern>
```

The `pattern` argument above is a regular expression of your desired address.
