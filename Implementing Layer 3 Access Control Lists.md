# Lab 3 : Implementing Layer 3 Access Control Lists (Perimeter Defense)

## Objective 
To implement & verify network layer (layer 3) traffic filtering mechanisms using Cisco Access Control Lists (ACLs), preventing unauthorized network segments from traversing the default gateway while maintaining connectivity for validated hosts.

## Topology Changes & Defensive Logic 
* **Context** Built directly on top of the established Layer 3 routing topology.
* **Mechanism** Configured an extended IP access control list on the default gateway router to inspect packet headers (source IP, destination IP, & protocol/port numbers)
* **Defensive Rule** Restrict traffic from untrusted network segments to sensitive server zones while explicitly permitting necessary administrative & protocol traffic. 

## Interface Configuration & Firewall Logic 
The router CLI was configured to enforce perimeter traffic constraints. 

