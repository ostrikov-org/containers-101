# would contain the layers, that when combined form the linux filesystem with alpine binaries
# i.e. /bin, /lib, /home, etc.
# as well as apk package manager
# this would be a SINGLE layer, since it is squashed
FROM alpine:3.12

# ONLY file1 is present on this layer
COPY file1.txt /

# ONLY file2 is present on this layer
COPY file2.txt /
