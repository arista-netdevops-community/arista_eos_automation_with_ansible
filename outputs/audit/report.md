Report generated with Ansible (Sun  3 May 2020 23:08:25 CEST)

# Audit report structure
[Report for device switch1.lab.local](#report-for-device-switch1lablocal)  
[Report for device switch2.lab.local](#report-for-device-switch2lablocal)  
[Report for device switch3.lab.local](#report-for-device-switch3lablocal)  
***************************************************
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
***************************************************
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
## Routing table (switch2)

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
***************************************************
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
## Routing table (switch3)

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
