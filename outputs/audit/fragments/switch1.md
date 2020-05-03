# Report for device switch1.lab.local

## Device details (switch1)

### HW model 

 

| Expected model | Actual model | Result |
| :-----: | :-----: | :-----: | 
| DCS-7150S-64-CL-F | DCS-7150S-64-CL-F | PASS |

### SW version 

 


| Expected version | Actual version | Result |
| :-----: | :-----: | :-----: | 
| 4.22.4M-2GB | 4.22.4M-2GB | PASS |

## Environment (switch1)  

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


## Interfaces admin and operationnal status (switch1)

### interfaces connected to other devices

| Interface | Admin status | Operationnal Status | Result |
| :-----: | :-----: | :-----: | :-----: | 
| Ethernet3 | up | up | PASS 
| Ethernet4 | up | up | PASS
## LLDP topology (switch1)
  
| Interface | Expected neighbor | Actual neighbor | Expected neighbor interface | Actual neighbor interface | Result |
| :-----: | :-----: | :-----: | :-----: | :-----: | :-----: | 
| Ethernet3 | switch2.lab.local | switch2.lab.local | Ethernet2 | Ethernet2 | PASS | 
| Ethernet4 | switch3.lab.local | switch3.lab.local | Ethernet2 | Ethernet2 | PASS |
## BGP (switch1)

###  EBGP sessions state
 
| EBGP Peer | Session state | Result |
| :-----: | :-----: | :-----: | 
| 10.10.10.1 | Established | PASS | 
| 10.10.10.3 | Established | PASS |
### IPv4 prefixes sent to EBGP peer 

 

| EBGP Peer | IPv4 Prefixes sent | Result |
| :-----: | :-----: | :-----: | 
| 10.10.10.1 | 5 | PASS | 
| 10.10.10.3 | 6 | PASS |
### IPv4 prefixes received from EBGP peer


| EBGP Peer | IPv4 Prefixes received | Result |
| :-----: | :-----: | :-----: | 
| 10.10.10.1 | 5 | PASS 
| 10.10.10.3 | 5 | PASS
## Routing table (switch1)

| Destination (EBGP peer loopback) | via next hop | via interface | Result |
| :-----: | :-----: | :-----: | :-----: | 
| 172.16.0.2/32 | 10.10.10.1 | Ethernet3 | PASS | 
| 172.16.0.3/32 | 10.10.10.3 | Ethernet4 | PASS |
## IP reachability (switch1)

### Ping EBGP peers from switch1 interfaces
 

| source interface | IP source | IP destination (EBGP peer) | Result |
| :-----: | :-----: | :-----: | :-----: | 
| Ethernet3 | 10.10.10.0  | 10.10.10.1 | PASS | 
| Ethernet4 | 10.10.10.2  | 10.10.10.3 | PASS |
### Ping EBGP peers loopback from switch1 interfaces

| source interface | IP source | IP destination (EBGP peer loopback) | Result |
| :-----: | :-----: | :-----: | :-----: | 
| Ethernet3 | 10.10.10.0  | 172.16.0.2 | PASS | 
| Ethernet4 | 10.10.10.2  | 172.16.0.3 | PASS |
### Ping EBGP peers loopback from switch1 loopback 
| IP source | IP destination (EBGP peer loopback) | Result |
| :-----: | :-----: | :-----: | 
| 172.16.0.1  | 172.16.0.2 | PASS | 
| 172.16.0.1  | 172.16.0.3 | PASS |
