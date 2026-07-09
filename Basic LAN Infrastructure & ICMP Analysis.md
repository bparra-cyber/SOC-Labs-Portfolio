

### Step 1: Physical Layer Setup (Topology)
*   **Hardware Selection:** Deployed two End Devices (bparra0 and bparra1) and connected them to a Cisco Catalyst 2960 Layer 2 switch. Chosen because it represents standard enterprise hardware rather than a generic simulation device.
*   **Media Connection:** Utilized Copper Straight-Through cabling to link the FastEthernet0 interfaces of the PCs to the FastEthernet0/1 and FastEthernet0/2 ports on the switch.
*   **Interface Observations:** Upon connection, noted link lights transition from orange to green. The orange state signifies Cisco's Spanning Tree Protocol (STP) actively inspecting the loop-free status of the port before transitioning to a forwarding state.
<img width="800" height="918" alt="image" src="https://github.com/user-attachments/assets/642a56b4-ddc2-4ce5-b54b-858790a7a1bc" />

### Step 2: Logical Addressing & Connectivity Verification
*   **Configuration:** Configured bparra0 with static IP `192.168.1.10` and bparra1 with `192.168.1.20`. Both utilize a `/24` subnet mask (`255.255.255.0`), placing them inside the same local network segment (`192.168.1.0`).
*   **Testing Tool:** Opened the command line interface on bparra0 and executed a network connectivity test using the standard `ping` utility directed at bparra1.
*   **Analysis of Results:** 
    *   The test successfully transmitted 4 ICMP Echo Request packets and received 4 corresponding Echo Replies from `192.168.1.20`.
    *   **0% packet loss** confirms a completely stable physical and logical path across the Layer 2 access switch.
    *   Round-trip times averaged `0ms`, indicative of local hardware-switched traffic with negligible propagation delay.
<img width="550" height="674" alt="image" src="https://github.com/user-attachments/assets/180f3dbe-f2ac-481e-83dc-180e22a732a7" />
