# Report for device switch3.lab.local

## Device details (switch3)

### HW model 

 

| Expected model | Actual model | Result |
| :-----: | :-----: | :-----: | 
| DCS-7150S-64-CL-F | DCS-7150S-64-CL-F | PASS |

### SW version 

 


| Expected version | Actual version | Result |
| :-----: | :-----: | :-----: | 
| 4.22.4M-2GB | 4.22.4M-2GB | PASS |

## Environment (switch3)  

### Power 

| Power Supply | State | Result |
| :-----: | :-----: | :-----: | 
| 1 | powerLoss | FAIL | 
| 2 | ok | PASS | 

### Temperature

 

| System temperature status| Result |
| :-----: | :-----: | 
| temperatureOk | PASS |

### Cooling

#### Power supplies 

| Power Supply | Fans status | Result |
| :-----: | :-----: | :-----: | 
| PowerSupply1 | ok | PASS | 
| PowerSupply2 | ok | PASS | 

#### Fan trays

| Fan tray | Fans status | Result |
| :-----: | :-----: | :-----: | 
| 1 | ok | PASS | 
| 2 | ok | PASS | 
| 3 | ok | PASS | 
| 4 | ok | PASS | 


## Interfaces admin and operationnal status (switch3)

### interfaces connected to other devices

| Interface | Admin status | Operationnal Status | Result |
| :-----: | :-----: | :-----: | :-----: | 
| Ethernet2 | up | up | PASS 
| Ethernet24 | up | up | PASS
## LLDP topology (switch3)
  
| Interface | Expected neighbor | Actual neighbor | Expected neighbor interface | Actual neighbor interface | Result |
| :-----: | :-----: | :-----: | :-----: | :-----: | :-----: | 
| Ethernet2 | switch1.lab.local | switch1.lab.local | Ethernet4 | Ethernet4 | PASS | 
| Ethernet24 | switch2.lab.local | switch2.lab.local | Ethernet24 | Ethernet24 | PASS |
## BGP (switch3)

###  EBGP sessions state
 
| EBGP Peer | Session state | Result |
| :-----: | :-----: | :-----: | 
| 10.10.10.2 | Established | PASS | 
| 10.10.10.4 | Established | PASS |
### IPv4 prefixes sent to EBGP peer 

 

| EBGP Peer | IPv4 Prefixes sent | Result |
| :-----: | :-----: | :-----: | 
| 10.10.10.2 | 5 | PASS | 
| 10.10.10.4 | 6 | PASS |
### IPv4 prefixes received from EBGP peer


| EBGP Peer | IPv4 Prefixes received | Result |
| :-----: | :-----: | :-----: | 
| 10.10.10.2 | 6 | PASS 
| 10.10.10.4 | 6 | PASS
### Routing table

| Destination (EBGP peer loopback) | via next hop | via interface | Result |
| :-----: | :-----: | :-----: | :-----: | 
| 172.16.0.1/32 | 10.10.10.2 | Ethernet2 | PASS | 
| 172.16.0.2/32 | 10.10.10.4 | Ethernet24 | PASS |
## IP reachability (switch3)

### Ping EBGP peers from switch3 interfaces
 

| source interface | IP source | IP destination (EBGP peer) | Result |
| :-----: | :-----: | :-----: | :-----: | 
| Ethernet2 | 10.10.10.3  | 10.10.10.2 | PASS | 
| Ethernet24 | 10.10.10.5  | 10.10.10.4 | PASS |
### Ping EBGP peers loopback from switch3 interfaces

| source interface | IP source | IP destination (EBGP peer loopback) | Result |
| :-----: | :-----: | :-----: | :-----: | 
| Ethernet2 | 10.10.10.3  | 172.16.0.1 | PASS | 
| Ethernet24 | 10.10.10.5  | 172.16.0.2 | PASS |
### Ping EBGP peers loopback from switch3 loopback 
| IP source | IP destination (EBGP peer loopback) | Result |
| :-----: | :-----: | :-----: | 
| 172.16.0.3  | 172.16.0.1 | PASS | 
| 172.16.0.3  | 172.16.0.2 | PASS |
