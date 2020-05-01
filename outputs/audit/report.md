Report generated with Ansible (Fri  1 May 2020 17:37:10 CEST)

# Report structure
[Report for device switch1.lab.local](#report-for-device-switch1.lab.local)  
[Report for device switch2.lab.local](#report-for-device-switch2.lab.local)  
[Report for device switch3.lab.local](#report-for-device-switch3.lab.local)  
***************************************************
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
***************************************************
# Report for device switch2.lab.local

## Device details
   

| Hostname | Model | Version |
| :-----: | :-----: | :-----: | 
| switch2 | DCS-7150S-64-CL-F | 4.22.4M-2GB |

## Interfaces admin and operationnal status 

### switch2 interfaces connected to other devices

| Interface | Admin status | operationnal Status | Result |
| :-----: | :-----: | :-----: | :-----: | 
| Ethernet2 | up | up | PASS 
| Ethernet24 | up | up | PASS
## LLDP topology (switch2)
  
| Interface | Expected neighbor | Expected neighbor interface | actual neighbor | actual neighbor interface | Result |
| :-----: | :-----: | :-----: | :-----: | :-----: | :-----: | 
| Ethernet2 | switch1.lab.local | Ethernet3 | switch1.lab.local | Ethernet3 | PASS | 
| Ethernet24 | switch3.lab.local | Ethernet24 | switch3.lab.local | Ethernet24 | PASS |
## BGP (switch2)

###  EBGP sessions state
 
| Peer | State | Result |
| :-----: | :-----: | :-----: | 
| 10.10.10.0 | Established | PASS | 
| 10.10.10.5 | Established | PASS |
### BGP prefixes
| Peer | IPv4 Prefixes sent | IPv4 Prefixes received | Result |
| :-----: | :-----: | :-----: | :-----: | 
| 10.10.10.0 | 5 | 5 | PASS 
| 10.10.10.5 | 6 | 6 | PASS
### Routing table
| EBGP peer loopback | via next hop | via interface | Result |
| :-----: | :-----: | :-----: | :-----: | 
| 172.16.0.1/32 | 10.10.10.0 | Ethernet2 | PASS | 
| 172.16.0.3/32 | 10.10.10.5 | Ethernet24 | PASS |
## IP reachability  

### Ping EBGP peers

| Source (switch2) | destination (EBGP peer) | Result |
| :-----: | :-----: | :-----: | 
| 10.10.10.1  | 10.10.10.0 | PASS | 
| 10.10.10.4  | 10.10.10.5 | PASS |
### Ping EBGP peers loopback
| Source (switch2) | Destination (EBGP peer loopback) | Result |
| :-----: | :-----: | :-----: | 
| 10.10.10.1  | 172.16.0.1 | PASS | 
| 10.10.10.4  | 172.16.0.3 | PASS |
### Ping EBGP peers loopback from switch2 loopback 
| Source (switch2 loopback) | Destination (EBGP peer loopback) | Result |
| :-----: | :-----: | :-----: | 
| 172.16.0.2  | 172.16.0.1 | PASS | 
| 172.16.0.2  | 172.16.0.3 | PASS |
***************************************************
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
