# HTTPS proxy

Useful for proxying http -> https if your setup only understands http / you don't want to bother with certificates.

## Build

`docker build -t https-proxy:1 .`

## Run

`docker run --rm -d -p 1000:80 -e PROXY_TARGET=https://github.com https-proxy:1`

Now you can access Github on `http://localhost:1000`

You can change port 1000 to whatever port you want (assuming it is free on your host) and obviously change PROXY_TARGET as well.

Generally speaking, running with port 80 gives the best results (-p 80:80).