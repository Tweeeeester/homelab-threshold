# Threshold
This server manages the network ingress / egress and routing related services.

## Services
For all externally facing services, use a port where "59" + 3 digit service number.

|  #  | Service                        | Application | Port  |
|:---:|:-------------------------------|:------------|:-----:|
| 000 | Docker Management              | Portainer   | 59000 |
| 001 | DNS                            | PiHole      | 59001 |
| 002 | Reverse Proxy                  | Caddy       | 59002 |
| 003 | Security Operations Monitoring |             | 59003 |
| 004 | VPN                            |             | 59004 |

## Setup
Clone code from github
```bash
cd /srv/
git clone https://github.com/Tweeeeester/homelab-threshold.git ./threshold
```

Copy .env files to server
```bash
scp ./pihole/pihole.env username@threshold:/srv/pihole/pihole.env
```

Run Services
```bash
docker compose -f /srv/threshold/docker-management/portainer.compose.yaml up -d

docker compose -f /srv/threshold/dns/pihole.compose.yaml up -d
```

