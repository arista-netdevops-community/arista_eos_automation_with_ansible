# Report for device switch1.lab.local

## Device details
   

| Hostname | Model | Version |
| :-----: | :-----: | :-----: | 
| switch1 | DCS-7150S-64-CL-F | 4.22.4M-2GB |

## Interfaces admin and operationnal status 

### switch1 interfaces connected to other devices

| Interface | Admin status | operationnal Status | Result |
| :-----: | :-----: | :-----: | :-----: | 
| Ethernet3 | up | up | PASS 
| Ethernet4 | up | up | PASS
## LLDP topology (switch1)
  
| Interface | Expected neighbor | Expected neighbor interface | actual neighbor | actual neighbor interface | Result |
| :-----: | :-----: | :-----: | :-----: | :-----: | :-----: | 
| Ethernet3 | switch2.lab.local | Ethernet2 | switch2.lab.local | Ethernet2 | PASS | 
| Ethernet4 | switch3.lab.local | Ethernet2 | switch3.lab.local | Ethernet2 | PASS |
## BGP (switch1)

###  EBGP sessions state
 
| Peer | State | Result |
| :-----: | :-----: | :-----: | 
| 10.10.10.1 | Established | PASS | 
| 10.10.10.3 | Established | PASS |
### BGP prefixes
| Peer | IPv4 Prefixes sent | IPv4 Prefixes received | Result |
| :-----: | :-----: | :-----: | :-----: | 
| 10.10.10.1 | 5 | 5 | PASS 
| 10.10.10.3 | 6 | 5 | PASS
### Routing table
| EBGP peer loopback | via next hop | via interface | Result |
| :-----: | :-----: | :-----: | :-----: | 
| 172.16.0.2/32 | 10.10.10.1 | Ethernet3 | PASS | 
| 172.16.0.3/32 | 10.10.10.3 | Ethernet4 | PASS |
## IP reachability  

### Ping EBGP peers

| Source (switch1) | destination (EBGP peer) | Result |
| :-----: | :-----: | :-----: | 
| 10.10.10.0  | 10.10.10.1 | PASS | 
| 10.10.10.2  | 10.10.10.3 | PASS |
### Ping EBGP peers loopback
| Source (switch1) | Destination (EBGP peer loopback) | Result |
| :-----: | :-----: | :-----: | 
| 10.10.10.0  | 172.16.0.2 | PASS | 
| 10.10.10.2  | 172.16.0.3 | PASS |
### Ping EBGP peers loopback from switch1 loopback 
| Source (switch1 loopback) | Destination (EBGP peer loopback) | Result |
| :-----: | :-----: | :-----: | 
| 172.16.0.1  | 172.16.0.2 | PASS | 
| 172.16.0.1  | 172.16.0.3 | PASS |
