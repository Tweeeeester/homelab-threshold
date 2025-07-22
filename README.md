# Threshold
This server manages the network ingress / egress and routing related services.

## Services
[pihole.env](dns/pihole.env)
For all externally facing services, use a port where "59" + 3 digit service number.

|  #  | Service                        | Port  | Notes      |
|:---:|:-------------------------------|:-----:|:-----------|
| 000 | Docker Management              | 59000 | Portainer  |
| 001 | DNS                            | 59001 | PiHole DNS |
| 002 | Reverse Proxy                  | 59002 |            |
| 003 | Security Operations Monitoring | 59003 |            |
| 004 | VPN                            | 59004 |            |

## Setup
Clone code from github
```bash
cd /srv/
git clone https://github.com/Tweeeeester/homelab-threshold.git .
```

Copy .env files to server
```bash
scp ./dns/pihole.env username@threshold:/srv/dns/pihole.env
```

Run Services
```bash
docker compose -f dns/pihole.compose.yaml up -d
```

