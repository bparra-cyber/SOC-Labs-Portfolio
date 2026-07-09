## Lab 2: Expanding the Network with a Layer 3 Router

### Objective
Introduce a default gateway to allow communication outside of the local network segment.

### Topology Changes
- Added a Cisco 1941 Router (`Router0`).
- Connected `Switch1` (port `Fa0/3`) to `Router0` (port `Gig0/0`) using a Copper Straight-Through cable.
<img width="905" height="645" alt="image" src="https://github.com/user-attachments/assets/12671275-5645-4408-93d8-7d9dba4a9589" />

### Interface Configuration
```ciscolog
Router>enable
Router#configure terminal
Router(config)#interface GigabitEthernet0/0
Router(config-if)#ip address 192.168.1.254 255.255.255.0
Router(config-if)#no shutdown
```

<img width="645" height="938" alt="image" src="https://github.com/user-attachments/assets/56d03d97-7c37-4892-b0d2-0a5cddbfd38c" />


