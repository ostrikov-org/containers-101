# Demonstrate how layers overlay

Build a sandbox image:
```bash
docker build . -t sandbox-image:latest
```

Export an image (in OCI format) to a tar.gz

It would contain all the necessary layers and metadata for us to inspect
```bash
docker save sandbox-image:latest -o sandbox-image.tar.gz
# if you have dive, inspect oci image
# if you don't, untar it
dive docker-archive://sandbox-image.tar.gz
```

# Other Useful commands
## Remove every docker image in the system
```bash
docker image rm `docker images --format="{{.ID}}"`
```
