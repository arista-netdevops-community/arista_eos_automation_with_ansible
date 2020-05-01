# Report for device switch3.lab.local

## Device details
   

| Hostname | Model | Version |
| :-----: | :-----: | :-----: | 
| switch3 | DCS-7150S-64-CL-F | 4.22.4M-2GB |

## Interfaces admin and operationnal status 

### switch3 interfaces connected to other devices

| Interface | Admin status | operationnal Status | Result |
| :-----: | :-----: | :-----: | :-----: | 
| Ethernet2 | up | up | PASS 
| Ethernet24 | up | up | PASS
## LLDP topology (switch3)
  
| Interface | Expected neighbor | Expected neighbor interface | actual neighbor | actual neighbor interface | Result |
| :-----: | :-----: | :-----: | :-----: | :-----: | :-----: | 
| Ethernet2 | switch1.lab.local | Ethernet4 | switch1.lab.local | Ethernet4 | PASS | 
| Ethernet24 | switch2.lab.local | Ethernet24 | switch2.lab.local | Ethernet24 | PASS |
## BGP (switch3)

###  EBGP sessions state
 
| Peer | State | Result |
| :-----: | :-----: | :-----: | 
| 10.10.10.2 | Established | PASS | 
| 10.10.10.4 | Established | PASS |
### BGP prefixes
| Peer | IPv4 Prefixes sent | IPv4 Prefixes received | Result |
| :-----: | :-----: | :-----: | :-----: | 
| 10.10.10.2 | 5 | 6 | PASS 
| 10.10.10.4 | 6 | 6 | PASS
### Routing table
| EBGP peer loopback | via next hop | via interface | Result |
| :-----: | :-----: | :-----: | :-----: | 
| 172.16.0.1/32 | 10.10.10.2 | Ethernet2 | PASS | 
| 172.16.0.2/32 | 10.10.10.4 | Ethernet24 | PASS |
## IP reachability  

### Ping EBGP peers

| Source (switch3) | destination (EBGP peer) | Result |
| :-----: | :-----: | :-----: | 
| 10.10.10.3  | 10.10.10.2 | PASS | 
| 10.10.10.5  | 10.10.10.4 | PASS |
### Ping EBGP peers loopback
| Source (switch3) | Destination (EBGP peer loopback) | Result |
| :-----: | :-----: | :-----: | 
| 10.10.10.3  | 172.16.0.1 | PASS | 
| 10.10.10.5  | 172.16.0.2 | PASS |
### Ping EBGP peers loopback from switch3 loopback 
| Source (switch3 loopback) | Destination (EBGP peer loopback) | Result |
| :-----: | :-----: | :-----: | 
| 172.16.0.3  | 172.16.0.1 | PASS | 
| 172.16.0.3  | 172.16.0.2 | PASS |
