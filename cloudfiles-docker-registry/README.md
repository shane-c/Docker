Cloud Files/Swift backend for Docker registry
======

Dockerfile for setting up a Rackspace Cloud Files/Swift backend for Docker registry. 

Build: docker build -rm -t swift-registry .

Use:
```
  docker run -d \
  -e SETTINGS_FLAVOR=swift \ 
  -e OS_CONTAINER=Cloud Files container name \
  -e OS_AUTH_URL=https://identity.api.rackspacecloud.com/v2.0/ \
  -e STORAGE_PATH=/ \
  -e OS_USERNAME=Cloud Account Username \
  -e OS_PASSWORD=Cloud Account Password \
  -e OS_TENANT_NAME=Cloud Account ID # \
  -e OS_REGION_NAME=Region (IAD, ORD, DFW, SYD, HKG) \
  -e SEARCH_BACKEND=sqlalchemy \
  -p 5000:5000 \
  swift-registry
```
