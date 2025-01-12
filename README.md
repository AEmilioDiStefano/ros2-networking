# SHOWING NETWORK INFORMATION IN A LINUX TERMINAL

### Print network information including:
Destination (IP address), Gateway, Genmask, Flags, MSS Window, irtt, Interface Name:

```bash
netstat -rn
```
### Show DNS Server:

```bash
nmcli device show wlp2s0 | grep IP4.DNS
```



