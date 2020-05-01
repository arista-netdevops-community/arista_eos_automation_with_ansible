# Report for device switch2.lab.local

## Device details (switch2)

### HW model 

 

| Expected model | Actual model | Result |
| :-----: | :-----: | :-----: | 
| DCS-7150S-64-CL-F | DCS-7150S-64-CL-F | PASS |

### SW version 

 


| Expected version | Actual version | Result |
| :-----: | :-----: | :-----: | 
| 4.22.4M-2GB | 4.22.4M-2GB | PASS |

## Environment (switch2)  

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


## Interfaces admin and operationnal status (switch2)

### interfaces connected to other devices

| Interface | Admin status | Operationnal Status | Result |
| :-----: | :-----: | :-----: | :-----: | 
| Ethernet2 | up | up | PASS 
| Ethernet24 | up | up | PASS
## LLDP topology (switch2)
  
| Interface | Expected neighbor | Actual neighbor | Expected neighbor interface | Actual neighbor interface | Result |
| :-----: | :-----: | :-----: | :-----: | :-----: | :-----: | 
| Ethernet2 | switch1.lab.local | switch1.lab.local | Ethernet3 | Ethernet3 | PASS | 
| Ethernet24 | switch3.lab.local | switch3.lab.local | Ethernet24 | Ethernet24 | PASS |
## BGP (switch2)

###  EBGP sessions state
 
| EBGP Peer | Session state | Result |
| :-----: | :-----: | :-----: | 
| 10.10.10.0 | Established | PASS | 
| 10.10.10.5 | Established | PASS |
### IPv4 prefixes sent to EBGP peer 

 

| EBGP Peer | IPv4 Prefixes sent | Result |
| :-----: | :-----: | :-----: | 
| 10.10.10.0 | 5 | PASS | 
| 10.10.10.5 | 6 | PASS |
### IPv4 prefixes received from EBGP peer


| EBGP Peer | IPv4 Prefixes received | Result |
| :-----: | :-----: | :-----: | 
| 10.10.10.0 | 5 | PASS 
| 10.10.10.5 | 6 | PASS
### Routing table

| Destination (EBGP peer loopback) | via next hop | via interface | Result |
| :-----: | :-----: | :-----: | :-----: | 
| 172.16.0.1/32 | 10.10.10.0 | Ethernet2 | PASS | 
| 172.16.0.3/32 | 10.10.10.5 | Ethernet24 | PASS |
## IP reachability (switch2)

### Ping EBGP peers from switch2 interfaces
 

| source interface | IP source | IP destination (EBGP peer) | Result |
| :-----: | :-----: | :-----: | :-----: | 
| Ethernet2 | 10.10.10.1  | 10.10.10.0 | PASS | 
| Ethernet24 | 10.10.10.4  | 10.10.10.5 | PASS |
### Ping EBGP peers loopback from switch2 interfaces

| source interface | IP source | IP destination (EBGP peer loopback) | Result |
| :-----: | :-----: | :-----: | :-----: | 
| Ethernet2 | 10.10.10.1  | 172.16.0.1 | PASS | 
| Ethernet24 | 10.10.10.4  | 172.16.0.3 | PASS |
### Ping EBGP peers loopback from switch2 loopback 
| IP source | IP destination (EBGP peer loopback) | Result |
| :-----: | :-----: | :-----: | 
| 172.16.0.2  | 172.16.0.1 | PASS | 
| 172.16.0.2  | 172.16.0.3 | PASS |
