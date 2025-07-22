# Installing Pihole in Docker

## Disable DNS
DNS might need to be disabled on the host system in order for docker to be able to bind to port 53.

To Disable:
```bash
sudo systemctl disable systemd-resolved.service
sudo systemctl stop systemd-resolved.service
```

Check and see if port 53 is taken:

```bash
lsof -i :53
```

OR

```bash
netstat -tulpn | grep ":53 "
```