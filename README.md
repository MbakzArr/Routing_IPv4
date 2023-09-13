# Routing_IPv4

This is a lab exercise for configuring OSPFv2 for IPv4 Routing using Cisco Packet Tracer. The lab involves configuring router interfaces and OSPFv2, setting up PC networks, and verifying connectivity.

## Getting Started

To get started with this lab, follow these steps:

- Start the Packet Tracer exercise named "SWRE_Module_14-15_Routing_IPv4_CiscoExercise.pkt."

### PC2 Network

1. Configured R2 interface Gig 0/0/0 with the address 200.129.2.2/24.
2. Examined the existing OSPF configuration on R2, then added the network 200.129.2.0/24.
3. Saved the configuration.
4. Configured PC2 with the address 200.129.2.9/24 and set R2 interface Gig 0/0/0 as the default gateway.
5. Verified that PC2 can ping all interfaces on R2 (200.129.2.2, 3.2.0.2, and 4.2.0.2).

### PC3 Network

1. Configured R3 interface Gig 0/0/0 with the address 200.129.3.3/24.
2. Examined the existing OSPF configuration on R3, then added the network 200.129.3.0/24.
3. Saved the configuration.
4. Configured PC3 with the address 200.129.3.9/24 and set R3 interface Gig 0/0/0 as the default gateway.
5. Verified that PC3 can ping all interfaces on R3 (200.129.3.3, 3.1.0.3, and 3.2.0.3).

### PC4 Network

1. Configured R4 interface Gig 0/0/0 with the address 200.129.4.4/24.
2. Examined the existing OSPF configuration on R4, then added the network 200.129.4.0/24.
3. Saved the configuration.
4. Configured PC4 with the address 200.129.4.9/24 and set R4 interface Gig 0/0/0 as the default gateway.
5. Verified that PC4 can ping all interfaces on R4 (200.129.4.4, 4.1.0.4, and 4.2.0.4).

### Confirm Basic OSPF Operation

1. Verified that PC4 can now ping PC3 and PC2.
2. Verified that each PC4 can ping R1 interface Gig 0/0/1 (4.1.0.1) and Gig 0/0/2 (3.1.0.1) but is not able to reach the Internet (9.9.9.9).

### Add a Default Route

1. On R1, Added a default route to ISP and configured OSPF to advertise that default route.
2. Saved the config on R1.
3. On R4, confirmed that R1 has advertised the OSPF default route and is using it as the "Gateway of last resort."

## Evaluation

The lab will be evaluated based on the following criteria:

### R1

- Has a default static route to ISP (200.1.1.9)
- Has an OSPF route to PC2 network (200.129.2.0/24)
- Has an OSPF route to PC3 network (200.129.3.0/24)
- Has an OSPF route to PC4 network (200.129.4.0/24)

### R2

- Has an OSPF default route (0.0.0.0/0)
- Has an OSPF route to PC3 network (200.129.3.0/24)
- Has an OSPF route to PC4 network (200.129.4.0/24)

### PC2

- Can ping R2 at 200.129.2.2
- Can ping PC3 at 200.129.3.9
- Can ping PC4 at 200.129.4.9
- Can ping ISP at 9.9.9.9

### PC4

- Can ping R4 at 200.129.4.4
- Can ping PC3 at 200.129.3.9
- Can ping ISP at 9.9.9.9
