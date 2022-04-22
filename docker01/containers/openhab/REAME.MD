From Dokumentation:
https://www.openhab.org/docs/installation/docker.html#obtaining-the-official-image-from-dockerhub

Create the openhab user
Just because one is running in an isolated container does not mean running as root is recommended. So first create an openhab user configured to be a system user with no home and no shell. This can be done on Ubuntu and Raspbian with the command:
```
sudo useradd -r -s /sbin/nologin openhab
usermod -a -G openhab <user>

sudo chown -R openhab:openhab /opt/container/openhab/data
```
