# Networking

### Subnet masking

The ip address eg-`192.168.0.1` in which the network prefix i.e. `192.168.0` helps to identify the network whereas the reamaining `.1` is a host identifier.  
The each group `192` is called the octet.  
to identify which part of ip address is the network prefix subnet mask is used.  
    Eg- `172.135.0.1` is the ip address and `255.128.0.0` now the addressess both are compared in binaries then ones of both addressess are matched is the network prefix and then remaining zeros are the host address.  
Like:
  ip     - 172.135.0.1 -> $\color{red}\text{10101100 01111110}$ 00000101 00000001  
  subnet - 255.128.0.0 -> $\color{red}\text{11111111 10000000}$ 00000000 00000000  
Now the bits in red defines which network it belongs to which remaining bits show the host address.
The subnet mask can only be in the range 0 128 192 224 240 248 252 254 255 only. And /8 represents 255.0.0.0 in same way /16 /24 /32 are known as `CIDR` notation.  

