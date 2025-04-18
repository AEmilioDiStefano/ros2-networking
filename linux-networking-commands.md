# SHOWING NETWORK INFORMATION IN A LINUX TERMINAL

### Lists all available network interfaces:
NOTE: WiFi interfaces are usually called "wlan0", "wlan1", "wlp2s0", or something similar beginning with "w".
```bash
ip addr
```
(also shows other information like IP Address, subnet mask, etc)

### Show all devices on an interface: 

```bash
sudo arp-scan -l --interface=<name_of_interface>
```
Replace ,name_of_interface> with the name of the interface which you would like to see the devices on.  For example, if your target interface is called "wlp2s0", then enter the following command:

```bash
sudo arp-scan -l --interface=wlp2s0
```

### Print network information including:
Destination (IP address), Gateway, Genmask, Flags, MSS Window, irtt, Interface Name:

```bash
netstat -rn
```
### Show DNS Server:

```bash
nmcli device show wlp2s0 | grep IP4.DNS
```

### Print only the Gateway:

```bash
ip route | grep default
```


