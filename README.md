# Threshold
This server manages the network ingress / egress and routing related services.

## Services

For all externally facing services, use a port where "59" + 3 digit service number.
Server / service admin interfaces start at "599"

|  #  | Service                        | Port  | Notes      |
|:---:|:-------------------------------|:-----:|:-----------|
| 000 | DNS                            | 59000 | PiHole DNS |
| 001 | Reverse Proxy                  | 59001 |            |
| 002 | Security Operations Monitoring | 59002 |            |
| 003 | VPN                            | 59003 |            |
| 901 | Docker Management              | 59901 | Portainer  |


