# directions range

private ip ranges:
- 10.0.0.0 /8
- 172.16.0.0 /12
- 192.168.0.0 /16

restricted ip address:
- 127.0.0.0 /8 -> loopback 

# basic concepts 

IP addres: 32 bits divided into 4 octets 

MAC address (Medium Access Control): unique identifier that identifies a device inside a network

subnet: determines on an IP address where the network ID ends and where the host ID begins
- CIDR notation: /24 = 255.255.255.0 -> 24 bits are for the network id, 32-24=8 are for hosts
- 2 directions are reserved for the network: first one for the ID and last one for broadcast messages

-> how many hosts can a network have?
2^n - 2, being n the number of bits free by a mask

"two devices can talk directly to each other if they have the same network id. if not, a router is needed."

default gateway: exit door for a device that is outside of its own subnet
-> "a device's default gateway MUST be an IP address on its own local subnet"

## devices
- switch (layer 2): connects devices **within the same network**. uses MAC addresses to forward data between computers
- router (layer 3): connects different networks through various interfaces

## OSI layer
- layer 1: physical streams of bits through cables
- layer 2 (data link): communication in local LAN through switches regarding MACs
- layer 3 (network): IP addresses and routing in different networks
- layer 4-7 (transport to application protocols): TCP/UDP ports, encryption, HTTP...
