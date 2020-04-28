Report generated with Ansible (Tue 28 Apr 2020 10:44:48 CEST)

## Report for device switch1

### Device details
   

| Hostname | domain name | Model | Version |
| :-----: | :-----: | :-----: | :-----: | 
| switch1 | lab.local | DCS-7150S-64-CL-F | 4.22.4M-2GB |

### Interfaces admin and operationnal status (switch1)

| Interface | Admin status | operationnal Status | Result |
| :-----: | :-----: | :-----: | :-----: | 
| Ethernet3 | up | up | PASS 
| Ethernet4 | up | up | PASS
### LLDP topology (switch1)
  
| Interface | Expected neighbor | Expected neighbor interface | actual neighbor | actual neighbor interface | Result |
| :-----: | :-----: | :-----: | :-----: | :-----: | :-----: | 
| Ethernet3 | switch2.lab.local | Ethernet2 | switch2.lab.local | Ethernet2 | PASS | 
| Ethernet4 | switch3.lab.local | Ethernet2 | switch3.lab.local | Ethernet2 | PASS |
### Ping EBGP peers (switch1)

| Source | destination | Result |
| :-----: | :-----: | :-----: | 
| 10.10.10.0  | 10.10.10.1 | PASS | 
| 10.10.10.2  | 10.10.10.3 | PASS |
###  BGP session state (switch1)
 
| Peer | State | Result |
| :-----: | :-----: | :-----: | 
| 10.10.10.1 | Established | PASS | 
| 10.10.10.3 | Established | PASS |
### BGP prefixes (switch1)
| Peer | Prefixes sent | Prefixes received | Result |
| :-----: | :-----: | :-----: | :-----: | 
| 10.10.10.1 | 6 | 5 | PASS 
| 10.10.10.3 | 5 | 5 | PASS
### Routing table (switch1)
| Address | via next hop | via interface | Result |
| :-----: | :-----: | :-----: | :-----: | 
| 172.16.0.2/32 | 10.10.10.1 | Ethernet3 | PASS | 
| 172.16.0.3/32 | 10.10.10.3 | Ethernet4 | PASS |
### Ping EBGP peers loopback (switch1)
| Source | Destination | Result |
| :-----: | :-----: | :-----: | :-----: | 
| 10.10.10.0  | 172.16.0.2 | PASS | 
| 10.10.10.2  | 172.16.0.3 | PASS |
### Ping EBGP peers loopback from switch1 loopback 
| Source | Destination | Result |
| :-----: | :-----: | :-----: | :-----: | 
| 172.16.0.1  | 172.16.0.2 | PASS | 
| 172.16.0.1  | 172.16.0.3 | PASS |
## Report for device switch2

### Device details
   

| Hostname | domain name | Model | Version |
| :-----: | :-----: | :-----: | :-----: | 
| switch2 | lab.local | DCS-7150S-64-CL-F | 4.22.4M-2GB |

### Interfaces admin and operationnal status (switch2)

| Interface | Admin status | operationnal Status | Result |
| :-----: | :-----: | :-----: | :-----: | 
| Ethernet2 | up | up | PASS 
| Ethernet24 | up | up | PASS
### LLDP topology (switch2)
  
| Interface | Expected neighbor | Expected neighbor interface | actual neighbor | actual neighbor interface | Result |
| :-----: | :-----: | :-----: | :-----: | :-----: | :-----: | 
| Ethernet2 | switch1.lab.local | Ethernet3 | switch1.lab.local | Ethernet3 | PASS | 
| Ethernet24 | switch3.lab.local | Ethernet24 | switch3.lab.local | Ethernet24 | PASS |
### Ping EBGP peers (switch2)

| Source | destination | Result |
| :-----: | :-----: | :-----: | 
| 10.10.10.1  | 10.10.10.0 | PASS | 
| 10.10.10.4  | 10.10.10.5 | PASS |
###  BGP session state (switch2)
 
| Peer | State | Result |
| :-----: | :-----: | :-----: | 
| 10.10.10.0 | Established | PASS | 
| 10.10.10.5 | Established | PASS |
### BGP prefixes (switch2)
| Peer | Prefixes sent | Prefixes received | Result |
| :-----: | :-----: | :-----: | :-----: | 
| 10.10.10.0 | 5 | 6 | PASS 
| 10.10.10.5 | 6 | 6 | PASS
### Routing table (switch2)
| Address | via next hop | via interface | Result |
| :-----: | :-----: | :-----: | :-----: | 
| 172.16.0.1/32 | 10.10.10.0 | Ethernet2 | PASS | 
| 172.16.0.3/32 | 10.10.10.5 | Ethernet24 | PASS |
### Ping EBGP peers loopback (switch2)
| Source | Destination | Result |
| :-----: | :-----: | :-----: | :-----: | 
| 10.10.10.1  | 172.16.0.1 | PASS | 
| 10.10.10.4  | 172.16.0.3 | PASS |
### Ping EBGP peers loopback from switch2 loopback 
| Source | Destination | Result |
| :-----: | :-----: | :-----: | :-----: | 
| 172.16.0.2  | 172.16.0.1 | PASS | 
| 172.16.0.2  | 172.16.0.3 | PASS |
