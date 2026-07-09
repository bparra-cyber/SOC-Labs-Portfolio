## Lab 2: Expanding the Network with a Layer 3 Router

### Objective
Introduce a default gateway to allow communication outside of the local network segment.

### Topology Changes
- Added a Cisco 1941 Router (`Router0`).
- Connected `Switch1` (port `Fa0/3`) to `Router0` (port `Gig0/0`) using a Copper Straight-Through cable.

### Interface Configuration
```ciscolog
Router>enable
Router#configure terminal
Router(config)#interface GigabitEthernet0/0
Router(config-if)#ip address 192.168.1.254 255.255.255.0
Router(config-if)#no shutdown
<img width="698" height="932" alt="image" src="https://github.com/user-attachments/assets/69a8f8a0-4d9f-482b-852d-cd8259ed29c4" />
