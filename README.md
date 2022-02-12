# HTTPS proxy

Useful for proxying http -> https if your setup only understands http / you don't want to bother with certificates.

## Build

`docker build -t https-proxy:1 .`

## Run

`docker run --rm -p 1000:80 -e PROXY_TARGET=https://github.com https-proxy:1`

Now you can access Github on `http://localhost:1000`
